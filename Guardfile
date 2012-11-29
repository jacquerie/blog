guard 'livereload' do
  watch(%r{content/pages(/.+)\.(mdown|textile|haml)}) { |match| match[1] }
  watch(%r{public(/.+\.(jpe?g|js|png))}) { |match| match[1] }
  watch(%r{views/.+\.haml})
  watch(%r{views/(.+)\.s[ac]ss}) do |match|
    if match[1] =~ /(mixins|variables)/
      ["/css/master.css", "/css/layout.css"]
    else
      "/css/#{match[1]}.css"
    end
  end
end

