php annotations
===============

php annotations like java

```
<?php

namespace Tests;

/**
 * @Dao
 * @Entity()
 * @InlineAnnotation("hello")
 * @InlineAnnotationWithNamedParams(param1 = "value1", param2 = "value2")
 * @MultilineAnnotation(
 * param1 = "hello"
 * )
 * @ArrayAnnotations([
 * "hello1",
 * "hello2",
 * ])
 * @ArrayParameterAnnotation(param = [
 * "hello1",
 * "hello2",
 * ])
 */
class Model
{

}
```

```
$annotationReader = new \phpenhance\Annotations\AnnotationReader(\Tests\Model::class);
$annotationReader->parse();

$annotations = $annotationReader->getAnnotations();
// TODO: ..

```