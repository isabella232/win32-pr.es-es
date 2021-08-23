---
description: TAPI 1.4 agregó una serie de API, mensajes, constantes y elementos de estructura a la especificación 1.3.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1.4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f22833639813268420cc1ea202ef260964b42ce2e5119fafc8d0aa18593686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060363"
---
# <a name="tapi-14"></a>TAPI 1.4

TAPI 1.4 agregó una serie de API, mensajes, constantes y elementos de estructura a la especificación 1.3. TAPI 1.4 solo admite TSP de 16 bits. Sin embargo, permite desarrollar aplicaciones de 32 bits sin tener que preocuparse por las limitaciones de las aplicaciones de 16 Windows.

Los archivos de encabezado TAPI y TSPI se usan para desarrollar ambas aplicaciones para TAPI 1.4 y TAPI 2.x. Aunque no hubo muchos cambios en las estructuras entre estas dos especificaciones, hubo cambios en la API (específicamente, compatibilidad con Unicode) que hacen que sea muy importante tener en cuenta que los encabezados se compilan de forma diferente, en función de la constante TAPI \_ CURRENT \_ VERSION. Por ejemplo:

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> TAPI \_ CURRENT VERSION debe \_ definirse para todas las aplicaciones TAPI. Aunque no es estrictamente necesario para el desarrollo de TAPI 2.x, podrían producirse cambios futuros para requerir esto.

 

 

 



