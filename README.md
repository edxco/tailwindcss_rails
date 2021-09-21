# Layout of Rails 6 and Tailwindcss 2.0
## Intended for development and production enviroment

This layout was created in order to work with webpack and be reused in future projects. I'm using this rails setup to deploy in an AWS EC2 instance.

Requirements:
 - Postgresql
 - Tailwindcss 2.0
 - Rails 6.1.4.1
 - Ruby 3.0.2

 Tailwind requires PostCSS 8, and Rails 6 has not updated yet. Thanks to their documentation, we can easily fix this issue by installing Tailwind's compatibility build. Just run the following to fix it:
```
 npm uninstall tailwindcss postcss autoprefixer
 npm install -D tailwindcss@npm:@tailwindcss/postcss7-compat @tailwindcss/postcss7-compat postcss@^7 autoprefixer@^9
```

How to run this project:
 - Clone project
 - Run bundle install
 - Run 'yarn add tailwindcss'
 - Create 'tailwindbase' role in postgresql
 - Run 'rails assets:precompile'
 - Run 'rails s -e production'
 