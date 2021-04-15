---
title: Versiones de sistema operativo
description: Este tipo de datos DWORD debe contener el tipo de sistema operativo en la palabra de orden superior y el número de versión del sistema operativo en la palabra de orden inferior. En la tabla siguiente se muestran los valores posibles para el sistema operativo.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Versiones de sistema operativo almacenamiento estructurado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665833"
---
# <a name="operating-system-versions"></a><span data-ttu-id="63040-105">Versiones de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="63040-105">Operating System Versions</span></span>

<span data-ttu-id="63040-106">Este tipo de datos **DWORD** debe contener el tipo de sistema operativo en la palabra de orden superior y el número de versión del sistema operativo en la palabra de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="63040-106">This **DWORD** data type should hold the operating system type in the high-order word and the version number of the operating system in the low-order word.</span></span> <span data-ttu-id="63040-107">En la tabla siguiente se muestran los valores posibles para el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="63040-107">Possible values for the operating system are listed in the following table.</span></span>



| <span data-ttu-id="63040-108">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="63040-108">Operating system</span></span>       | <span data-ttu-id="63040-109">Value</span><span class="sxs-lookup"><span data-stu-id="63040-109">Value</span></span>  |
|------------------------|--------|
| <span data-ttu-id="63040-110">Windows de 32 bits (Win32)</span><span class="sxs-lookup"><span data-stu-id="63040-110">32-Bit Windows (Win32)</span></span> | <span data-ttu-id="63040-111">0x0002</span><span class="sxs-lookup"><span data-stu-id="63040-111">0x0002</span></span> |
| <span data-ttu-id="63040-112">Macintosh</span><span class="sxs-lookup"><span data-stu-id="63040-112">Macintosh</span></span>              | <span data-ttu-id="63040-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="63040-113">0x0001</span></span> |
| <span data-ttu-id="63040-114">Windows de 16 bits (Win16)</span><span class="sxs-lookup"><span data-stu-id="63040-114">16-Bit Windows (Win16)</span></span> | <span data-ttu-id="63040-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="63040-115">0x0000</span></span> |



 

<span data-ttu-id="63040-116">En el caso de los sistemas operativos Microsoft Windows, la versión del sistema operativo es la palabra de orden inferior devuelta por la función [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) .</span><span class="sxs-lookup"><span data-stu-id="63040-116">For Microsoft Windows operating systems, the operating system version is the low-order word returned by the [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) function.</span></span> <span data-ttu-id="63040-117">En el caso de Microsoft Windows, el código de ejemplo siguiente establece correctamente la versión del sistema operativo de origen.</span><span class="sxs-lookup"><span data-stu-id="63040-117">For Microsoft Windows, the following example code correctly sets the version of the originating operating system.</span></span>

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 