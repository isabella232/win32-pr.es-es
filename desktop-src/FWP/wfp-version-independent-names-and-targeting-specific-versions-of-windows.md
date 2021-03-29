---
title: Los nombres de Version-Independent de WFP y el destino de versiones específicas de Windows
description: En muchos casos, la API de la plataforma de filtrado de Windows (WFP) proporciona más de una versión de una función o estructura.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665593"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a>Los nombres de Version-Independent de WFP y el destino de versiones específicas de Windows

En muchos casos, la API de la plataforma de filtrado de Windows (WFP) proporciona más de una versión de una función o estructura.

La mayoría de los nombres de datos y funciones de la API de WFP finalizan con un número de versión, como "0" o "1", incluso si solo hay una versión.

## <a name="version-mapping-in-fwpvih"></a>Asignación de versión en fwpvi. h

El archivo de encabezado fwpvi. h se incluye a partir del SDK de Windows 7 y WDK. Este archivo de encabezado asigna el nombre de la API sin versión a la versión adecuada para su uso con un sistema operativo determinado.

Por ejemplo, a continuación se muestra un extracto breve de la versión de fwpvi. h que se incluye en el SDK de Windows 8.


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



Como se mostró anteriormente, solo hay una versión de **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) , por lo que cualquier llamada a **FwpmNetEventCreateEnumHandle** llamará siempre a **FwpmNetEventCreateEnumHandle0**, independientemente del sistema operativo de destino.

Sin embargo, hay tres versiones de **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)y [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2). El archivo de encabezado fwpvi. h garantiza que una llamada a **FwpmNetEventEnum** llamará a la versión más adecuada para el sistema operativo de destino:

-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) para Windows 8 (o posterior)
-   El destino de [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) para Windows 7 es
-   [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) para sistemas operativos anteriores (como Windows Vista o Windows Vista con Service Pack 1 (SP1))

## <a name="calling-version-independent-functions-and-structures"></a>Llamar a funciones y estructuras de Version-Independent

Se recomienda a los desarrolladores de WFP que tengan como destino un sistema operativo o una versión de WDK determinados programar siempre en las macros independientes de la versión. Se seleccionará automáticamente la versión más reciente admitida en el sistema operativo al que se destina. Se recomienda el uso de los archivos de encabezado más recientes, incluso cuando el destino es un sistema operativo anterior. De este modo, se asegurará de que se utiliza la última versión compatible y también podrá facilitar el mantenimiento y la actualización del código.

La [documentación de referencia](fwp-reference.md) de la API de WFP describe cada versión de una API numerada. Si existe más de una versión, se indica el sistema operativo de destino. Sin embargo, los desarrolladores normalmente querrán llamar a las API independientes de la versión (sin número) e indicar el sistema operativo de destino (por ejemplo, **NTDDI \_ WIN6** para Windows Vista o **NTDDI \_ WIN8** para Windows 8).

Para garantizar el control correcto de las funciones que toman parámetros diferentes en versiones diferentes, puede incluir bloques condicionales como `#if (NTDDI_VERSION >= NTDDI_WIN7)` .

 

 




