# PHP - Good Practises

## [Writing Beautiful Code](https://dev.to/restoreddev/writing-beautiful-code-10p6)

- start with a unit test (its helps us know how we want the code to be shaped)

```php
class EmailClientTest extends \PHPUnit\Framework\TestCase
{
    public function test_sending_an_email()
    {
        $client = new \Email\Client();
        $emailMessage = new \Email\Message('Hello world!');

        $result = $client->send('andrew@dev.to', $emailMessage);

        $this->assertTrue($result);
    }
}
```

- use nouns for class names and verbs for methods (see above example)
- keep functions small
- use a style guide (such as [PSR-2](https://www.php-fig.org/psr/psr-2/))