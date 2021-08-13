---
description: 'Al crear una instancia con objetos incrustados, realice las siguientes tareas:'
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: Crear objetos incrustados
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2e54e16005669ebd77b0bc08e5d3174f7aa5fadee2a47477920e91aaa2ae155b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464175"
---
# <a name="creating-embedded-objects"></a>Crear objetos incrustados

Al crear una instancia con objetos incrustados, realice las siguientes tareas:

-   Debe declarar un objeto incrustado como fuertemente con tipo o con tipos débiles.

    Un objeto fuertemente con tipo apunta a un objeto de una clase específica y usa el nombre de clase. Un objeto débilmente con tipo apunta a un objeto de una clase sin especificar y usa la palabra **clave object.** Ambos objetos se asignan al **tipo VT \_ UNKNOWN.**

-   Puede usar **NULL para el** valor predeterminado de objetos incrustados y rutas de acceso en inicializaciones y declaraciones.
-   Al insertar una ruta de acceso de objeto, no coloque espacios en blanco entre los elementos de la ruta de acceso incrustada. Por ejemplo, la ruta de acceso del objeto "Class1Index=3;" no contiene espacio entre el nombre de propiedad "Class1index" y el valor que se asigna, que es "3".

En la siguiente declaración de clase se muestra cómo declarar objetos incrustados fuertemente con tipo y con tipos débiles.

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

En los ejemplos siguientes se describe cómo declarar objetos incrustados dentro de una declaración de clase.

``` syntax
Class Class1 
{ 
     [key] sint32 Class1Index;
};

Class Class2 
{
    [key] sint32 Class2Index;
    Class1 EmbedObject1 = instance of Class1{Class1Index=3;};
};

Class Class3
{
    [key] sint32 Class3Index;
    Class2 EmbedObject2 = instance of Class2 {Class2Index=4;};
};
```

En el ejemplo siguiente se describe la inicialización de una propiedad que es un objeto fuertemente con tipo y otra propiedad que es una matriz de objetos con tipos débiles.

``` syntax
Class EmbedClass1
{
    [key] sint32 intval;
};

Class EmbedClass2
{
    [key] string sval;
};

Class ContainerClass
{
    [key] sint32 intval;
    EmbedClass1 SingleObject;
    Object ArrayObject[];
};

Instance of ContainerClass
{
    intval = 33;
    SingleObject = instance of EmbedClass1 {intval=99;};
    ArrayObject = {instance of EmbedClass2 {sval="something";},
                   instance of EmbedClass1 {intval=100;}};
};
```

 

 



