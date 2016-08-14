### Chapter 1
Exercise 1:
```
file = File.read('test.txt')
puts file

puts "This file has #{file.split.length} words"
puts "And #{file.split.uniq.lenght} unique words"
```

Exercise 2:
```
words = file.split(' ')
count = Hash.new(0)
words.each { |word| count[word] +=1}
```
Exercise 3:
```
class WordCounter
   def count
     @file.split.length
   end
   def uniq_count
     @file.split.uniq.count
   end
   def count_words
     count = Hash.new(0)
     words = @file.split
     words.each { |word| count[word.downcase] +=1}
     count
   end
end

test = WordCounter.new('test.txt')
test.count
test.uniq_count
test.count_words
```
