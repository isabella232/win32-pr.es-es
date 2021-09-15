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
ms.openlocfilehash: a76a70fa0e01068622a4f4cdbbbfb6c992b67f56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466376"
---
# <a name="creating-embedded-objects"></a>Crear objetos incrustados

Al crear una instancia con objetos incrustados, realice las siguientes tareas:

-   Debe declarar un objeto incrustado como fuertemente con tipo o con tipos débiles.

    Un objeto fuertemente tipo apunta a un objeto de una clase específica y usa el nombre de clase. Un objeto débilmente con tipo apunta a un objeto de una clase no especificada y usa la palabra **clave object.** Ambos objetos se asignan al **tipo \_ VT UNKNOWN.**

-   Puede usar **NULL para el** valor predeterminado de los objetos incrustados y las rutas de acceso en las inicializaciones y declaraciones.
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

 

 



