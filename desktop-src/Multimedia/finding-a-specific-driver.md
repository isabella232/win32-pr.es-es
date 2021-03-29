---
title: Búsqueda de un controlador específico
description: Búsqueda de un controlador específico
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- Administrador de compresión de audio (ACM), buscar controladores
- ACM (Administrador de compresión de audio), buscar controladores
- Ejemplos de ACM, buscar controladores
- Buscar controladores
- acmDriverEnum función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903779"
---
# <a name="finding-a-specific-driver"></a><span data-ttu-id="9db91-108">Búsqueda de un controlador específico</span><span class="sxs-lookup"><span data-stu-id="9db91-108">Finding a Specific Driver</span></span>

<span data-ttu-id="9db91-109">Es posible que desee que la aplicación envíe un mensaje directamente a un controlador específico o que identifique determinados controladores de la lista.</span><span class="sxs-lookup"><span data-stu-id="9db91-109">You might want your application to send a message directly to a specific driver or to identify certain drivers from the list.</span></span> <span data-ttu-id="9db91-110">Por ejemplo, puede que desee que la aplicación identifique los controladores que admiten filtros y, a continuación, consulte cada controlador para determinar las etiquetas de filtro que admite.</span><span class="sxs-lookup"><span data-stu-id="9db91-110">For example, you might want your application to identify those drivers that support filters and then query each driver to determine which filter tags it supports.</span></span> <span data-ttu-id="9db91-111">Puede usar la función [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) para obtener un identificador para el controlador o los controladores que desee; Este identificador se puede usar para comunicarse con el controlador.</span><span class="sxs-lookup"><span data-stu-id="9db91-111">You can use the [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) function to obtain a handle to the desired driver or drivers; this handle can then be used to communicate with that driver.</span></span>

<span data-ttu-id="9db91-112">Tenga en cuenta que cuando una aplicación instala un controlador local para su propio uso, la función [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) devuelve un identificador de controlador, que se puede usar para comunicarse con el controlador.</span><span class="sxs-lookup"><span data-stu-id="9db91-112">Note that when an application installs a local driver for its own use, the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function returns a driver handle, which can be used to communicate with the driver.</span></span> <span data-ttu-id="9db91-113">En este caso, no es necesario usar **acmDriverEnum** .</span><span class="sxs-lookup"><span data-stu-id="9db91-113">It is not necessary to use **acmDriverEnum** in this case.</span></span>

 

 




