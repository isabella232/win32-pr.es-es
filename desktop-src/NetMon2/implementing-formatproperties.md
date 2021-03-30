---
description: Monitor de red llama a la función FormatProperties para dar formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de Monitor de red.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implementación de FormatProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660b581bf29fd8e5d40af65f5ff90e1e9223ad2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154144"
---
# <a name="implementing-formatproperties"></a>Implementación de FormatProperties

Monitor de red llama a la función [**FormatProperties**](formatproperties.md) para dar formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de monitor de red. Normalmente, se llama a **FormatProperties** para dar formato a la línea de Resumen de un protocolo y, a continuación, para dar formato a todas las instancias de propiedad del protocolo dentro de un marco. Sin embargo, Monitor de red no identifica el número de veces que se llama a **FormatProperties** para un analizador específico.

Al llamar a [**FormatProperties**](formatproperties.md), monitor de red proporciona una estructura [**PROPERTYINST**](propertyinst.md) para cada propiedad que muestra. La estructura **PROPERTYINST** proporciona información sobre los datos que se van a mostrar, incluido un puntero a la estructura [**PROPERTYINFO**](propertyinfo.md) que especifica la función que se va a utilizar para dar formato a la propiedad de datos mostrada.

> [!Note]  
> Cuando se agrega una propiedad a la base de datos de [*propiedades*](p.md) del analizador, se especifica una estructura [**PROPERTYINFO**](propertyinfo.md) .

 

Monitor de red identifica la función de formato que se va a llamar para cada instancia de propiedad. El miembro **InstanceData** de la estructura [**PROPERTYINFO**](propertyinfo.md) puede especificar lo siguiente:

-   La función [**FormatPropertyInstance**](formatpropertyinstance.md) para usar el [*formateador genérico*](g.md) que proporciona monitor de red.

    -O bien-

-   Nombre de una función de formato personalizado que proporciona el analizador.

Las funciones de formato personalizado y [**FormatPropertyInstance**](formatpropertyinstance.md) devuelven los datos con formato que se muestran en el panel de detalles de la interfaz de usuario de monitor de red.

En la ilustración siguiente se muestra cómo Monitor de red identifica la función a la que se va a llamar para cada instancia de propiedad.

![Cómo identifica el monitor de red la función a la que se va a llamar](images/formatprop1.png)

En el procedimiento siguiente se identifican los pasos necesarios para implementar [**FormatProperties**](formatproperties.md).

**Para implementar FormatProperties**

-   Con una estructura de bucle, llame a la función Format para cada estructura [**PROPERTYINST**](propertyinst.md) que se pasa al analizador en el parámetro *lpPropInst* de la función [**FormatProperties**](formatproperties.md) .

La siguiente es una implementación básica de [**FormatProperties**](formatproperties.md).

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

 

 



