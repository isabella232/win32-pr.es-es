---
description: El tipo de datos OBJECT es un objeto de clase WMI que se usa para declarar asociaciones con establecimiento flexible de tipos y objetos incrustados.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c257b45833204a873292da467d484fab97b22b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808287"
---
# <a name="object"></a><span data-ttu-id="392fc-103">OBJECT</span><span class="sxs-lookup"><span data-stu-id="392fc-103">OBJECT</span></span>

<span data-ttu-id="392fc-104">El tipo de datos OBJECT es un objeto de clase WMI que se usa para declarar asociaciones con establecimiento flexible de tipos y objetos incrustados.</span><span class="sxs-lookup"><span data-stu-id="392fc-104">The OBJECT data type is a WMI class object use to declare weakly typed associations and embedded objects.</span></span> <span data-ttu-id="392fc-105">No defina la clase específica para un objeto débilmente tipado hasta que cree una instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="392fc-105">You do not define the specific class for a weakly typed object until you create an instance of the class.</span></span> <span data-ttu-id="392fc-106">Los objetos incrustados definidos con el tipo de datos OBJECT pueden contener instancias de cualquier clase WMI.</span><span class="sxs-lookup"><span data-stu-id="392fc-106">Embedded objects defined with the OBJECT data type can contain instances of any WMI class.</span></span> <span data-ttu-id="392fc-107">Para obtener más información, vea [objetos incrustados](embedded-objects.md).</span><span class="sxs-lookup"><span data-stu-id="392fc-107">For more information, see [Embedded Objects](embedded-objects.md).</span></span>

<span data-ttu-id="392fc-108">En el ejemplo siguiente se definen y crean instancias de dos clases, una de las cuales contiene un objeto incrustado de tipo OBJECT:</span><span class="sxs-lookup"><span data-stu-id="392fc-108">The following example defines and creates instances of two classes, one of which contains an embedded object of type OBJECT:</span></span>

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

 

 



