# twig_reflection

## Objectives

This Twig extension allows to access public static attributes and methods of a class.

## Installation

1. Copy the file **__Reflection.php__** in the **__Twig/Extension__** directory of your Bundle/Module.
2. Declare the extension. For example in Symfony 2/3, you have to do it in the **__app/config/services.yml__** :
```
site.twig.reflectionExtension:
        class: AppBundle\Twig\Extension\Reflection
        tags:
            - { name: twig.extension } 
```
## Utilization
There are two methods callable in this extension :
```
* callStaticMethod($className, $methodName, array $args = [])
```
```
* getStaticAttribute($className, $attributeName)
```

From your Twig template, just call the good one with the proper parameters, for example:
```
set arrType = getStaticAttribute('AppBundle\\Entity\\Book', 'arrSearchTypes')
```
