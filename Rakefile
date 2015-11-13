namespace :mail do
  require 'mail'

  task :setup_client do
    Mail.defaults do
      delivery_method :smtp, {
        address: 'smtp.sendgrid.net',
        port: '587',
        domain: 'heroku.com',
        user_name: ENV['SENDGRID_USERNAME'],
        password: ENV['SENDGRID_PASSWORD'],
        authentication: :plain,
        enable_starttls_auto: true,
      }
    end
  end

  task :send, [:to, :body] => [:setup_client] do |t, args|
    Mail.deliver do
      to args[:to]
      from 'no-reply@termin.monitor'
      subject 'Bürgeramt slot available!'
      html_part do
        content_type 'text/html; charset=UTF-8'
        body args[:body]
      end
    end
  end
end
