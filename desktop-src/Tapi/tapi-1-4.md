---
description: TAPI 1,4 agregó varias API, mensajes, constantes y elementos de estructura a la especificación 1,3.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001923"
---
# <a name="tapi-14"></a>TAPI 1,4

TAPI 1,4 agregó varias API, mensajes, constantes y elementos de estructura a la especificación 1,3. TAPI 1,4 solo admite profesionales de 16 bits. Sin embargo, permite desarrollar aplicaciones de 32 bits sin tener que preocuparse por las limitaciones de Windows de 16 bits.

Los archivos de encabezado TAPI y TSPI se utilizan para desarrollar ambas aplicaciones tanto para TAPI 1,4 como para TAPI 2. x. Aunque no hubo muchos cambios en las estructuras entre estas dos especificaciones, hubo cambios en la API (específicamente, compatibilidad con Unicode) que hacen que sea muy importante tener en cuenta que los encabezados se compilan de forma diferente, dependiendo de la constante de la \_ versión actual de TAPI \_ . Por ejemplo:

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> La \_ \_ versión actual de TAPI debe definirse para todas las aplicaciones TAPI. Aunque no es estrictamente necesario para el desarrollo de TAPI 2. x, pueden producirse cambios futuros para requerir este problema.

 

 

 



