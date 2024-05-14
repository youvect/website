require "html-proofer"

task :clean do
  sh "rm -rf _site"
  sh "rm -rf .bundle"
  sh "rm -rf .jekyll-cache"
  sh "rm Gemfile.lock"
end

task :test do
  sh "bundle exec jekyll build"
  options = {
    ignore_empty_alt: false,
    ignore_status_codes: [
      999
    ]
  }
  HTMLProofer.check_directory("./_site", options).run
end
