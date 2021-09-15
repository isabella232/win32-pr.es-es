---
description: El tipo de datos OBJECT es un objeto de clase WMI que se usa para declarar asociaciones débilmente con tipo y objetos incrustados.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c257b45833204a873292da467d484fab97b22b0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465698"
---
# <a name="object"></a>OBJECT

El tipo de datos OBJECT es un objeto de clase WMI que se usa para declarar asociaciones débilmente con tipo y objetos incrustados. No se define la clase específica para un objeto con tipos débiles hasta que se crea una instancia de la clase . Los objetos incrustados definidos con el tipo de datos OBJECT pueden contener instancias de cualquier clase WMI. Para obtener más información, vea [Objetos incrustados.](embedded-objects.md)

En el ejemplo siguiente se definen y crean instancias de dos clases, una de las cuales contiene un objeto incrustado de tipo OBJECT:

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

class CompositeClass
{
    [key] string aKey;   
    object EmbObj;       // Weakly typed
};

class EmbClass

{
  [key] string aKey;
};

instance of CompositeClass
{
    aKey = "CompositeClass Key";
    EmbObj = 
        instance of EmbClass
        {
           aKey = "key for embedded object";
        };
};
```

 

 



