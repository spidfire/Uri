# Uri
Uri library for PHP

```
<?php
namespace 

$uri = new Uri('http://example.com');

$uri->setPath('test')->toUrl(); // http://example.com/test
$uri->append('test')->toUrl(); // http://example.com/test
$uri->append('test','15')->toUrl();  // http://example.com/test/15
$uri->append('test','/#/')->toUrl();  // http://example.com/test/%2F%23%2F
$uri->appendTemplate('test/{id}/',['id' => 15])->toUrl();  // http://example.com/test/15/
$uri->addQuery('q',test)->toUrl();  // http://example.com/?q=test
$uri->setHash('test')->toUrl();  // http://example.com/#test
$uri->setQueryArray(['q' => 'test'])->toUrl();  // http://example.com/?q=test
$uri->setQueryArray(['q' => 'test'])->toUrl();  // http://example.com/?q=test


$uri2 = $uri
->appendTemplate('test/{id}/',['id' => 15])
->setHash('test')
->setQueryArray(['q' => 'test'])->toUrl();

$uri2->getScheme(); // http
$uri2->getDomain(); // example.com
$uri2->getQuery(); // ['q' => 'test']
$uri2->getHash(); // test
$uri2->getTld(); // com
$uri2->getPath(); // test/15/
$uri2->getPathParts(); // ['test' ,'15']



```
