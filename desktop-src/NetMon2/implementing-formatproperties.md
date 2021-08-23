---
description: Monitor de red llama a la función FormatProperties para dar formato a los datos que se muestran en el panel de detalles de la interfaz Monitor de red usuario.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implementar FormatProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50e7b927f15ccb2c216e345b37bc87593e33339671f906e28d33759ca9db0abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778984"
---
# <a name="implementing-formatproperties"></a>Implementar FormatProperties

Monitor de red llama a la [**función FormatProperties**](formatproperties.md) para dar formato a los datos que se muestran en el panel de detalles de la interfaz Monitor de red usuario. Normalmente, se llama a **FormatProperties** para dar formato a la línea de resumen de un protocolo y, a continuación, para dar formato a todas las instancias de propiedad del protocolo dentro de un marco. Sin embargo, Monitor de red no identifica el número de veces que se llama a **FormatProperties** para un analizador específico.

Al llamar [**a FormatProperties**](formatproperties.md), Monitor de red proporciona una [**estructura PROPERTYINST**](propertyinst.md) para cada propiedad que muestra. La **estructura PROPERTYINST** proporciona información sobre los datos que se van a mostrar, incluido un puntero a la estructura [**PROPERTYINFO**](propertyinfo.md) que especifica la función que se va a usar para dar formato a la propiedad de datos mostrada.

> [!Note]  
> Se [**especifica una estructura PROPERTYINFO**](propertyinfo.md) al agregar una propiedad a la base de datos de [*propiedades*](p.md) del analizador.

 

Monitor de red identifica la función de formato a la que se llamará para cada instancia de propiedad. El **miembro InstanceData** de la [**estructura PROPERTYINFO**](propertyinfo.md) puede especificar lo siguiente:

-   La [**función FormatPropertyInstance**](formatpropertyinstance.md) para usar el [*formateador genérico*](g.md) que Monitor de red proporciona.

    -O bien-

-   Nombre de una función de formato personalizado que proporciona el analizador.

Las [**funciones FormatPropertyInstance**](formatpropertyinstance.md) y de formato personalizado devuelven los datos con formato que se muestran en el panel de detalles de la interfaz Monitor de red usuario.

En la ilustración siguiente se muestra Monitor de red identifica la función a la que se va a llamar para cada instancia de propiedad.

![cómo el monitor de red identifica la función a la que se va a llamar](images/formatprop1.png)

El procedimiento siguiente identifica los pasos necesarios para implementar [**FormatProperties.**](formatproperties.md)

**Para implementar FormatProperties**

-   Mediante una estructura de bucle, llame a la función format para cada estructura [**PROPERTYINST**](propertyinst.md) que se pasa al analizador en el parámetro *lpPropInst* de la [**función FormatProperties.**](formatproperties.md)

A continuación se muestra una implementación básica de [**FormatProperties.**](formatproperties.md)

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



