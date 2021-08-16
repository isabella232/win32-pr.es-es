---
description: El tipo de datos OBJECT es un objeto de clase WMI que se usa para declarar asociaciones con tipos débiles y objetos incrustados.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c26b8b6ff77f788aeed607057541d19d80fea4c105b53d492c1f1e8468b319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554936"
---
# <a name="object"></a>OBJECT

El tipo de datos OBJECT es un objeto de clase WMI que se usa para declarar asociaciones con tipos débiles y objetos incrustados. No se define la clase específica para un objeto con tipos débiles hasta que se crea una instancia de la clase . Los objetos incrustados definidos con el tipo de datos OBJECT pueden contener instancias de cualquier clase WMI. Para obtener más información, vea [Objetos incrustados.](embedded-objects.md)

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

 

 



