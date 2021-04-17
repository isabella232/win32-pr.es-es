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
# <a name="performance-dll-samples"></a><span data-ttu-id="0fa93-103">Ejemplos de DLL de rendimiento</span><span class="sxs-lookup"><span data-stu-id="0fa93-103">Performance DLL Samples</span></span>

<span data-ttu-id="0fa93-104">El Windows SDK (WSDK) contiene tres archivos dll completos de rendimiento de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0fa93-104">The Windows SDK (WSDK) contains three complete sample performance DLLs.</span></span> <span data-ttu-id="0fa93-105">Estos ejemplos se encuentran en el directorio Samples \\ Winbase \\ WinNT \\ PerfTool \\ PerfDlls</span><span class="sxs-lookup"><span data-stu-id="0fa93-105">These samples are located in the Samples\\WinBase\\WinNT\\PerfTool\\PerfDlls directory.</span></span> <span data-ttu-id="0fa93-106">La raíz de esta ruta de acceso es el directorio de instalación base de WSDK.</span><span class="sxs-lookup"><span data-stu-id="0fa93-106">The root of this path is the base installation directory of the WSDK.</span></span> <span data-ttu-id="0fa93-107">Puede descargar WSDK del [Kit de desarrollo de software (SDK) de Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (busque Windows SDK y seleccione la descarga del sistema operativo más reciente).</span><span class="sxs-lookup"><span data-stu-id="0fa93-107">You can download the WSDK from the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (search for Windows SDK and select the download for the latest released operating system).</span></span>

<span data-ttu-id="0fa93-108">Los ejemplos contenidos en este directorio son:</span><span class="sxs-lookup"><span data-stu-id="0fa93-108">The samples contained in this directory are:</span></span>

-   <span data-ttu-id="0fa93-109">**AppMem**: proporciona homólogos de las funciones [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)y [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) que notifican la información de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0fa93-109">**AppMem**—Provides counterparts of the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc), and [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) functions that report performance information.</span></span> <span data-ttu-id="0fa93-110">Los contadores de rendimiento del registro y la herramienta de rendimiento pueden leer la información de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0fa93-110">Performance counters in the registry and the Performance tool can read the performance information.</span></span>
-   <span data-ttu-id="0fa93-111">**LeakyBin**: muestra el uso de contadores de rendimiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0fa93-111">**LeakyBin**—Demonstrates the use of application performance counters.</span></span>
-   <span data-ttu-id="0fa93-112">**PerfGen**: proporciona tres perfiles de forma de onda en cinco períodos diferentes para su uso con la herramienta de rendimiento con el fin de proporcionar datos con una tasa y un valor conocidos.</span><span class="sxs-lookup"><span data-stu-id="0fa93-112">**PerfGen**—Provides three waveforms at five different periods for use with the Performance tool to provide data at a known rate and value.</span></span> <span data-ttu-id="0fa93-113">Esto puede ser útil para probar aplicaciones que usan datos de rendimiento y necesitan valores predecibles para realizar pruebas.</span><span class="sxs-lookup"><span data-stu-id="0fa93-113">This can be useful in testing applications that use performance data and need predictable values to test against.</span></span>

 

 
