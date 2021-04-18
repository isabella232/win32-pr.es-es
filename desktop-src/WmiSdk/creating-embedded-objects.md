---
description: 'Al crear una instancia de con objetos incrustados, realice las siguientes tareas:'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706931"
---
# <a name="creating-embedded-objects"></a><span data-ttu-id="4838d-103">Crear objetos incrustados</span><span class="sxs-lookup"><span data-stu-id="4838d-103">Creating Embedded Objects</span></span>

<span data-ttu-id="4838d-104">Al crear una instancia de con objetos incrustados, realice las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="4838d-104">When creating an instance with embedded objects, perform the following tasks:</span></span>

-   <span data-ttu-id="4838d-105">Debe declarar un objeto incrustado con establecimiento inflexible de tipos o con tipo débil.</span><span class="sxs-lookup"><span data-stu-id="4838d-105">You must declare an embedded object as strongly typed or weakly typed.</span></span>

    <span data-ttu-id="4838d-106">Un objeto fuertemente tipado apunta a un objeto de una clase específica y utiliza el nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="4838d-106">A strongly typed object points to an object of a specific class and uses the class name.</span></span> <span data-ttu-id="4838d-107">Un objeto débilmente tipado apunta a un objeto de una clase no especificada y utiliza la palabra clave **Object** .</span><span class="sxs-lookup"><span data-stu-id="4838d-107">A weakly typed object points to an object of an unspecified class and uses the **object** keyword.</span></span> <span data-ttu-id="4838d-108">Ambos objetos se asignan al tipo **\_ desconocido de VT** .</span><span class="sxs-lookup"><span data-stu-id="4838d-108">Both objects map to the **VT\_UNKNOWN** type.</span></span>

-   <span data-ttu-id="4838d-109">Puede usar **null** para el valor predeterminado de los objetos incrustados y las rutas de acceso en las inicializaciones y declaraciones.</span><span class="sxs-lookup"><span data-stu-id="4838d-109">You can use **NULL** for the default value of embedded objects and paths in initializations and declarations.</span></span>
-   <span data-ttu-id="4838d-110">Al incrustar una ruta de objeto, no coloque un espacio en blanco entre los elementos de la ruta de acceso incrustada.</span><span class="sxs-lookup"><span data-stu-id="4838d-110">When embedding an object path, do not place white space between the elements of the embedded path.</span></span> <span data-ttu-id="4838d-111">Por ejemplo, la ruta de acceso del objeto "Class1Index = 3;" no contiene ningún espacio entre el nombre de la propiedad "Class1index" y el valor que se asigna, que es "3".</span><span class="sxs-lookup"><span data-stu-id="4838d-111">For example, the object path "Class1Index=3;" contains no space between the property name "Class1index" and the value being assigned, which is "3".</span></span>

<span data-ttu-id="4838d-112">La siguiente declaración de clase muestra cómo declarar objetos incrustados fuertemente tipados y con establecimiento débil de tipos.</span><span class="sxs-lookup"><span data-stu-id="4838d-112">The following class declaration shows you how to declare strongly typed and weakly typed embedded objects.</span></span>

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

<span data-ttu-id="4838d-113">En los ejemplos siguientes se describe cómo declarar objetos incrustados dentro de una declaración de clase.</span><span class="sxs-lookup"><span data-stu-id="4838d-113">The following examples describe how to declare embedded objects within a class declaration.</span></span>

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

<span data-ttu-id="4838d-114">En el ejemplo siguiente se describe la inicialización de una propiedad que es un objeto fuertemente tipado y otra propiedad que es una matriz de objetos con establecimiento débil.</span><span class="sxs-lookup"><span data-stu-id="4838d-114">The following example describes the initialization of one property that is a strongly typed object and another property that is an array of weakly typed objects.</span></span>

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

 

 



