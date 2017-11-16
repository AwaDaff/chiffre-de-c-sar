def shift_char(c, base, offset)
  (((c.ord - base) + offset) % 26 + base).chr
end

def cipher(s, offset)
  s.chars.map do |c|
    case c
    when 'a'..'z'
      shift_char(c, 'a'.ord, offset)
    when 'A'..'Z'
      shift_char(c, 'A'.ord, offset)
    else
      c
    end
  end.join
end

cipher_text = cipher('what a string!', 5)
p cipher_text       # "Abj vf gur gvzr sbe nyy tbbq zra..."
original_text = cipher(cipher_text, 5)
p original_text     # "What a string!"
