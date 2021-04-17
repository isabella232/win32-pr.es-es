---
description: El Windows SDK (WSDK) contiene tres archivos dll completos de rendimiento de ejemplo.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Ejemplos de DLL de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667263"
---
# <a name="performance-dll-samples"></a>Ejemplos de DLL de rendimiento

El Windows SDK (WSDK) contiene tres archivos dll completos de rendimiento de ejemplo. Estos ejemplos se encuentran en el directorio Samples \\ Winbase \\ WinNT \\ PerfTool \\ PerfDlls La raíz de esta ruta de acceso es el directorio de instalación base de WSDK. Puede descargar WSDK del [Kit de desarrollo de software (SDK) de Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (busque Windows SDK y seleccione la descarga del sistema operativo más reciente).

Los ejemplos contenidos en este directorio son:

-   **AppMem**: proporciona homólogos de las funciones [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)y [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) que notifican la información de rendimiento. Los contadores de rendimiento del registro y la herramienta de rendimiento pueden leer la información de rendimiento.
-   **LeakyBin**: muestra el uso de contadores de rendimiento de la aplicación.
-   **PerfGen**: proporciona tres perfiles de forma de onda en cinco períodos diferentes para su uso con la herramienta de rendimiento con el fin de proporcionar datos con una tasa y un valor conocidos. Esto puede ser útil para probar aplicaciones que usan datos de rendimiento y necesitan valores predecibles para realizar pruebas.

 

 
