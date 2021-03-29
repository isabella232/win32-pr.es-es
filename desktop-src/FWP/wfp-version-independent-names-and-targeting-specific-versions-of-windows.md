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
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a><span data-ttu-id="f2446-103">Los nombres de Version-Independent de WFP y el destino de versiones específicas de Windows</span><span class="sxs-lookup"><span data-stu-id="f2446-103">WFP Version-Independent Names and Targeting Specific Versions of Windows</span></span>

<span data-ttu-id="f2446-104">En muchos casos, la API de la plataforma de filtrado de Windows (WFP) proporciona más de una versión de una función o estructura.</span><span class="sxs-lookup"><span data-stu-id="f2446-104">In many cases, the Windows Filtering Platform (WFP) API provides more than one version of a function or structure.</span></span>

<span data-ttu-id="f2446-105">La mayoría de los nombres de datos y funciones de la API de WFP finalizan con un número de versión, como "0" o "1", incluso si solo hay una versión.</span><span class="sxs-lookup"><span data-stu-id="f2446-105">Most data and function names in the WFP API end with a version number, such as "0" or "1", even if there is only one version.</span></span>

## <a name="version-mapping-in-fwpvih"></a><span data-ttu-id="f2446-106">Asignación de versión en fwpvi. h</span><span class="sxs-lookup"><span data-stu-id="f2446-106">Version Mapping in fwpvi.h</span></span>

<span data-ttu-id="f2446-107">El archivo de encabezado fwpvi. h se incluye a partir del SDK de Windows 7 y WDK.</span><span class="sxs-lookup"><span data-stu-id="f2446-107">The fwpvi.h header file is included starting with the Windows 7 SDK and WDK.</span></span> <span data-ttu-id="f2446-108">Este archivo de encabezado asigna el nombre de la API sin versión a la versión adecuada para su uso con un sistema operativo determinado.</span><span class="sxs-lookup"><span data-stu-id="f2446-108">This header file maps the versionless API name to the version that is appropriate for use with a given operating system.</span></span>

<span data-ttu-id="f2446-109">Por ejemplo, a continuación se muestra un extracto breve de la versión de fwpvi. h que se incluye en el SDK de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f2446-109">For example, here is a brief excerpt from the version of fwpvi.h included in the Windows 8 SDK.</span></span>


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



<span data-ttu-id="f2446-110">Como se mostró anteriormente, solo hay una versión de **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) , por lo que cualquier llamada a **FwpmNetEventCreateEnumHandle** llamará siempre a **FwpmNetEventCreateEnumHandle0**, independientemente del sistema operativo de destino.</span><span class="sxs-lookup"><span data-stu-id="f2446-110">As shown above, there is only one version of **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – so any call to **FwpmNetEventCreateEnumHandle** will always call **FwpmNetEventCreateEnumHandle0**, regardless of the operating system targeted.</span></span>

<span data-ttu-id="f2446-111">Sin embargo, hay tres versiones de **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)y [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span><span class="sxs-lookup"><span data-stu-id="f2446-111">However, there are three versions of of **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1), and [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span></span> <span data-ttu-id="f2446-112">El archivo de encabezado fwpvi. h garantiza que una llamada a **FwpmNetEventEnum** llamará a la versión más adecuada para el sistema operativo de destino:</span><span class="sxs-lookup"><span data-stu-id="f2446-112">The fwpvi.h header file ensures that a call to **FwpmNetEventEnum** will call the version most appropriate to the targeted operating system:</span></span>

-   <span data-ttu-id="f2446-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) para Windows 8 (o posterior)</span><span class="sxs-lookup"><span data-stu-id="f2446-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) for Windows 8 (or later)</span></span>
-   <span data-ttu-id="f2446-114">El destino de [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) para Windows 7 es</span><span class="sxs-lookup"><span data-stu-id="f2446-114">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) for Windows 7 is targeted</span></span>
-   <span data-ttu-id="f2446-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) para sistemas operativos anteriores (como Windows Vista o Windows Vista con Service Pack 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="f2446-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) for earlier operating systems (such as Windows Vista or Windows Vista with Service Pack 1 (SP1))</span></span>

## <a name="calling-version-independent-functions-and-structures"></a><span data-ttu-id="f2446-116">Llamar a funciones y estructuras de Version-Independent</span><span class="sxs-lookup"><span data-stu-id="f2446-116">Calling Version-Independent Functions and Structures</span></span>

<span data-ttu-id="f2446-117">Se recomienda a los desarrolladores de WFP que tengan como destino un sistema operativo o una versión de WDK determinados programar siempre en las macros independientes de la versión.</span><span class="sxs-lookup"><span data-stu-id="f2446-117">WFP developers targeting a particular operating system or WDK version are encouraged to always program against the version-independent macros.</span></span> <span data-ttu-id="f2446-118">Se seleccionará automáticamente la versión más reciente admitida en el sistema operativo al que se destina.</span><span class="sxs-lookup"><span data-stu-id="f2446-118">This will automatically select the latest version supported in the operating system you are targeting.</span></span> <span data-ttu-id="f2446-119">Se recomienda el uso de los archivos de encabezado más recientes, incluso cuando el destino es un sistema operativo anterior.</span><span class="sxs-lookup"><span data-stu-id="f2446-119">Use of the most recent header files is recommended, even when targeting an earlier operating system.</span></span> <span data-ttu-id="f2446-120">De este modo, se asegurará de que se utiliza la última versión compatible y también podrá facilitar el mantenimiento y la actualización del código.</span><span class="sxs-lookup"><span data-stu-id="f2446-120">Doing this consistently will ensure the latest supported version is used, and can also make it easier to maintain and update your code.</span></span>

<span data-ttu-id="f2446-121">La [documentación de referencia](fwp-reference.md) de la API de WFP describe cada versión de una API numerada.</span><span class="sxs-lookup"><span data-stu-id="f2446-121">The [WFP API reference documentation](fwp-reference.md) describes each version of a numbered API.</span></span> <span data-ttu-id="f2446-122">Si existe más de una versión, se indica el sistema operativo de destino.</span><span class="sxs-lookup"><span data-stu-id="f2446-122">If more than one version exists, the targeted operating system is noted.</span></span> <span data-ttu-id="f2446-123">Sin embargo, los desarrolladores normalmente querrán llamar a las API independientes de la versión (sin número) e indicar el sistema operativo de destino (por ejemplo, **NTDDI \_ WIN6** para Windows Vista o **NTDDI \_ WIN8** para Windows 8).</span><span class="sxs-lookup"><span data-stu-id="f2446-123">However, developers will generally want to call the version-independent (numberless) APIs, and indicate the targeted operating system (such as **NTDDI\_WIN6** for Windows Vista or **NTDDI\_WIN8** for Windows 8).</span></span>

<span data-ttu-id="f2446-124">Para garantizar el control correcto de las funciones que toman parámetros diferentes en versiones diferentes, puede incluir bloques condicionales como `#if (NTDDI_VERSION >= NTDDI_WIN7)` .</span><span class="sxs-lookup"><span data-stu-id="f2446-124">To ensure proper handling of functions that take different parameters in different versions, you can include conditional blocks such as `#if (NTDDI_VERSION >= NTDDI_WIN7)`.</span></span>

 

 




