---
description: El WINDOWS SDK (WSDK) contiene tres archivos DLL de rendimiento de ejemplo completos.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Ejemplos de DLL de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169137"
---
# <a name="performance-dll-samples"></a>Ejemplos de DLL de rendimiento

El WINDOWS SDK (WSDK) contiene tres archivos DLL de rendimiento de ejemplo completos. Estos ejemplos se encuentran en el directorio \\ Ejemplos de \\ WinBase WinNT \\ PerfTool \\ PerfDlls. La raíz de esta ruta de acceso es el directorio de instalación base del WSDK. Puede descargar el WSDK desde el Kit de desarrollo de [software (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) de Microsoft Windows (busque el SDK de Windows y seleccione la descarga del sistema operativo más reciente).

Los ejemplos contenidos en este directorio son:

-   **AppMem:** proporciona homólogos de las funciones [**GlobalAlloc,**](/windows/desktop/api/winbase/nf-winbase-globalalloc) [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)y [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) que informan de la información de rendimiento. Los contadores de rendimiento del Registro y la herramienta Rendimiento pueden leer la información de rendimiento.
-   **LeakyBin:** muestra el uso de contadores de rendimiento de aplicaciones.
-   **PerfGen:** proporciona tres formas de onda en cinco períodos diferentes para su uso con la herramienta rendimiento para proporcionar datos a una velocidad y un valor conocidos. Esto puede ser útil para probar aplicaciones que usan datos de rendimiento y necesitan valores de predicción para realizar pruebas.

 

 
