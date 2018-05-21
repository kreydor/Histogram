# histogram program to output letter frequency
puts "Text to analyze please: " 
text = gets.chomp

letters = text.split(//) 
#splits words into letters

frequencies = Hash.new(0)
# puts into hashmap each letter

letters.each { |letters| frequencies[letters] += 1 }
=begin
iterates through each letter (key) and assigns frequency (value)
=end

frequencies = frequencies.sort_by {|a, b| a }
frequencies.delete_if { |a, b| a ==" " }
=begin
sorted Alphabetically, Alternatively I could have used 
frequencies = frequencies.sort_by {|a, b| b }
to sort by the value instead of the key
=end


frequencies.each { |letters, frequency| puts letters + " - " + frequency.to_s }
