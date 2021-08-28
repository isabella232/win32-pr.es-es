---
title: Nombres de Version-Independent WFP y versiones específicas de destino de Windows
description: En muchos casos, la API Windows Filtering Platform (WFP) proporciona más de una versión de una función o estructura.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf5fbef08c3284d94eb215e0cce2fc44fc9b827b686e531057db22b60020132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766675"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a>Nombres de Version-Independent WFP y versiones específicas de destino de Windows

En muchos casos, la API Windows Filtering Platform (WFP) proporciona más de una versión de una función o estructura.

La mayoría de los nombres de datos y funciones de la API de WFP terminan con un número de versión, como "0" o "1", aunque solo haya una versión.

## <a name="version-mapping-in-fwpvih"></a>Asignación de versiones en fwpvi.h

El archivo de encabezado fwpvi.h se incluye a partir del SDK Windows 7 y WDK. Este archivo de encabezado asigna el nombre de la API sin versión a la versión adecuada para su uso con un sistema operativo determinado.

Por ejemplo, este es un breve extracto de la versión de fwpvi.h incluida en Windows 8 SDK.


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



Como se ha mostrado anteriormente, solo hay una versión de **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0,**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) por lo que cualquier llamada a **FwpmNetEventCreateEnumHandle** siempre llamará a **FwpmNetEventCreateEnumHandle0**, independientemente del sistema operativo de destino.

Sin embargo, hay tres versiones de **FwpmNetEventEnum:** [**FwpmNetEventEnum0,**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)y [**FwpmNetEventEnum2.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) El archivo de encabezado fwpvi.h garantiza que una llamada a **FwpmNetEventEnum llamará** a la versión más adecuada para el sistema operativo de destino:

-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) para Windows 8 (o posterior)
-   [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) para Windows 7 es el destino
-   [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) para sistemas operativos anteriores (como Windows Vista o Windows Vista con Service Pack 1 (SP1))

## <a name="calling-version-independent-functions-and-structures"></a>Llamar a Version-Independent funciones y estructuras

Se recomienda a los desarrolladores de WFP que tienen como destino un sistema operativo determinado o una versión de WDK programar siempre con las macros independientes de la versión. Esto seleccionará automáticamente la versión más reciente admitida en el sistema operativo de destino. Se recomienda usar los archivos de encabezado más recientes, incluso cuando el destino es un sistema operativo anterior. Si lo hace de forma coherente, se asegurará de que se usa la versión compatible más reciente y también puede facilitar el mantenimiento y actualización del código.

En la documentación de referencia de la API de [WFP](fwp-reference.md) se describe cada versión de una API numerada. Si existe más de una versión, se anota el sistema operativo de destino. Sin embargo, los desarrolladores generalmente querrán llamar a las API independientes de la versión (sin número) e indicar el sistema operativo de destino (como **NTDDI \_ WIN6** para Windows Vista o **NTDDI \_ WIN8** para Windows 8).

Para garantizar un control adecuado de las funciones que toman parámetros diferentes en distintas versiones, puede incluir bloques condicionales como `#if (NTDDI_VERSION >= NTDDI_WIN7)` .

 

 




