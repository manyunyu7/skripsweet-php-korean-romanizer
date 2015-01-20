korean-romanizer
================

PHP 5.4+ library to romanize Korean in UTF-8 format.

Description
===========

Uses the <strong>"[Revised Romanization of Korean (국어의 로마자 표기법)](http://www.korean.go.kr/eng/roman/roman.jsp)"</strong> which is the official Korean language romanization system in South Korea proclaimed by Ministry of Culture, Sports and Tourism. [Wikipedia page](http://en.wikipedia.org/wiki/Revised_Romanization_of_Korean). 

Notice that this is different from <strong>transliteration</strong>, which comes implemented in PHP's [intl extension](http://php.net/manual/en/book.intl.php) ([Transliterator class](http://php.net/manual/en/class.transliterator.php)).
For example, "왕십리" subway stop is transliterated as "wangsibli" but romanized as "wangsimni" (which is closer to the Korean pronuntiation).

Usage
=====
First add this library as requirement in your composer.json file. If you are not familiar with Composer, please read [its documentation](https://getcomposer.org/doc/01-basic-usage.md) first.

    {
      "require": {
        "liopic/korean-romanizer": "~1.0"
      }
    }

Then create a new KoreanRomanizer\Romanizer() instance with the Korean text in UTF-8 you want to romanize.
For example:
  
    require "vendor/autoload.php";
    
    $example = new KoreanRomanizer\Romanizer("안녕 하세요");
    echo $example->romanize(); //Displays "annyeong haseyo"

