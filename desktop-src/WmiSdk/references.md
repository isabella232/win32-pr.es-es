---
description: La palabra clave ref de MOF describe una ruta de acceso de objeto y se asigna a un tipo de \_ automatización BSTR de VT.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Referencias (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30722910de761f3d2111a3218cf364f49ccb3c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063939"
---
# <a name="references-wmi"></a>Referencias (WMI)

La palabra clave **ref** de MOF describe una ruta de acceso de objeto y se asigna a un tipo de \_ automatización BSTR de VT. La ruta de acceso del objeto puede ser una ruta de acceso completa a un servidor y un espacio de nombres, o una ruta de acceso relativa a otro objeto del mismo espacio de nombres. Puede usar una palabra **clave ref** para vincular dos o más clases. WMI admite dos tipos de rutas de acceso de objeto, que usan para definir rutas de acceso generales o específicas dentro de WMI.

El propósito principal de la **palabra clave ref** es reducir el tiempo de transporte y la codificación entre objetos que existen completamente en el repositorio WMI. También puede usar la palabra **clave ref** para crear una asociación entre dos clases. Para obtener más información, vea [Declarar una clase de asociación](declaring-an-association-class.md). Si el elemento al que se hace referencia se encuentra en el mismo archivo MOF, use un alias para inicializar el **valor ref.** Para obtener más información, vea [Crear un alias](creating-an-alias.md).

> [!Note]  
> Cuando se **aplica una** palabra de clave ref a una propiedad de clave, puede distinguir las referencias de objeto por el valor de cadena de objeto en lugar de por el valor desreferenciado.

 

MOF admite el concepto de una ruta de acceso de objeto fuertemente con tipos débiles y fuertemente tipo. Una ruta de acceso de objeto débilmente escrita apunta a un objeto de una clase no especificada y usa la palabra **clave ref** con la palabra [clave OBJECT.](object.md) Un objeto fuertemente con tipo apunta a un objeto de una clase específica y usa **ref** con el nombre de clase. En el ejemplo siguiente se describe una referencia **RefToAnyClass** débilmente con tipo que puede apuntar a cualquier clase o instancia de clase, y una referencia **RefToClassX** que solo puede apuntar a una clase o instancia **classX:**

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

En el ejemplo siguiente se describen dos instancias y un objeto de asociación que hace referencia a las instancias anteriores:

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 



