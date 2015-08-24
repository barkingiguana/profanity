task :test do
  original_words = File.readlines 'words.txt'
  unique_words = original_words.uniq
  if original_words.size != unique_words.size
    raise "Duplicate words detected"
  end
  puts "No duplicate words"

  sorted_words = original_words.sort
  original_words.each.with_index do |w1,i|
    w2 = sorted_words[i]
    if w1 != w2
      raise "Please keep words.txt in alphabetical order"
    end
  end
  puts "Words sorted alphabetically"

  puts "Everything good"
end

task default: :test
