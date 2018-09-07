# iOS-Useful-Links

## [SwiftLint](https://github.com/realm/SwiftLint)
A tool to enforce Swift style and conventions, loosely based on [GitHub's Swift Style Guide](https://github.com/github/swift-style-guide).

## [SwiftGen](https://github.com/SwiftGen/SwiftGen)
SwiftGen is a tool to auto-generate Swift code for resources of your projects, to make them type-safe to use.

## [Copy-Paste-Detector](https://medium.com/@nvashanin/%D0%B8%D0%BD%D1%82%D0%B5%D0%B3%D1%80%D0%B8%D1%80%D1%83%D0%B5%D0%BC-copy-paste-detector-%D0%B4%D0%BB%D1%8F-swift-%D0%B2-xcode-9ae87c20748)
Add [cpd_script.php](https://github.com/yakobz/iOS-Useful-Links/blob/master/cpd_script.php) file to your project, and add this run script:
```
# Running CPD
pmd cpd --files ${EXECUTABLE_NAME} --minimum-tokens 50 --language swift --encoding UTF-8 --format net.sourceforge.pmd.cpd.XMLRenderer > cpd-output.xml --failOnViolation true
# Running script
php ./cpd_script.php -cpd-xml cpd-output.xml
```
This script uses pmd. Installing via [Homebrew](http://brew.sh/): `brew install pmd`

## [Searching unused swift functions](https://github.com/PaulTaykalo/swift-scripts)
Add [unused.rb](https://github.com/yakobz/iOS-Useful-Links/blob/master/unused.rb) file to your project, and add this run script:
```
file="unused.rb"
if [ -f "$file" ]
then
echo "$file found."
ruby unused.rb xcode
else
echo "unused.rb doesn't exist"
fi
```
