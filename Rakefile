namespace :book do

  desc 'build basic book formats'
  task :build do
    puts "Converting to HTML..."
    `bundle exec asciidoctor openelectronics.asciidoc`
    puts " -- HTML output at openelectronics.html"

    puts "Converting to EPub..."
    `bundle exec asciidoctor-epub3 openelectronics.asciidoc`
    puts " -- Epub output at openelectronics.epub"

    puts "Converting to Mobi (kf8)..."
    `bundle exec asciidoctor-epub3 -a ebook-format=kf8 openelectronics.asciidoc`
    puts " -- Mobi output at openelectronics.mobi"

    puts "Converting to PDF... (this one takes a while)"
    `bundle exec asciidoctor-pdf openelectronics.asciidoc 2>/dev/null`
    puts " -- PDF  output at openelectronics.pdf"
  end
end
