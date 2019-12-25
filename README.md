# 8-Helpful-JavaScript-Snippets-String

8 Helpful JavaScript Snippets String 
## 1. byteSize: 
Trả về độ dài của String theo byte

const byteSize = str => new Blob([str]).size;

byteSize('😀'); // 4
byteSize('Hello World'); // 11
## 2. capitalize: 

Viết hoa chữ cái đầu tiên của câu

const capitalize = ([first, ...rest]) =>
  first.toUpperCase() + rest.join('');
  
capitalize('fooBar'); // 'FooBar'
capitalize('fooBar', true); // 'Foobar'
## 3. capitalizeEveryWord: 

Viết hoa chữ cái đầu tiên của mỗi từ

const capitalizeEveryWord = str => str.replace(/\b[a-z]/g, char => char.toUpperCase());

capitalizeEveryWord('hello world!'); // 'Hello World!'
## 4. decapitalize: 

chữ cái viết thường

const decapitalize = ([first, ...rest]) =>
  first.toLowerCase() + rest.join('')

decapitalize('FooBar'); // 'fooBar'
decapitalize('FooBar'); // 'fooBar'
## 5 . splitLines: 

Tách một chuỗi nhiều dòng thành một mảng hàng.

Sử dụng String.prototype.split() biểu thức chính quy để khớp với dòng mới và tạo một mảng.
const splitLines = str => str.split(/\r?\n/);

splitLines('This\nis a\nmultiline\nstring.\n'); // ['This', 'is a', 'multiline', 'string.' , '']
## 6 . stripHTMLTags 

Xóa thẻ HTML / XML ra khỏi string cho trước. Sử dụng biểu thức chính quy để xóa HTML / XMLthẻ khỏi chuỗi .

const stripHTMLTags = str => str.replace(/<[^>]*>/g, '');

stripHTMLTags('<p><em>lorem</em> <strong>ipsum</strong></p>'); // 'lorem ipsum'
## 7. sortCharactersInString 

Đoạn mã này có thể được sử dụng để sắp xếp theo thứ tự abc các ký tự trong một chuỗi.

const sortCharactersInString = str => [...str].sort((a, b) => a.localeCompare(b)).join('');

sortCharactersInString('cabbage'); // 'aabbceg'
## 8. words 

Đoạn mã này convert String thành một Array

const words = (str, pattern = /[^a-zA-Z-]+/) => str.split(pattern).filter(Boolean);

words('I love javaScript!!'); // ["I", "love", "javaScript"]
words('python, javaScript & coffee'); // ["python", "javaScript", "coffee"]
