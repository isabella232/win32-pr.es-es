---
title: Funciones de cliente DRM de Microsoft Windows Media
description: Funciones de cliente DRM de Microsoft Windows Media
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Media Format SDK, funciones
- Administración de derechos digitales (DRM), funciones
- DRM (administración de derechos digitales), funciones
- API extendidas del cliente DRM, funciones
- API extendidas de cliente, funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705089"
---
# <a name="microsoft-windows-media-drm-client-functions"></a><span data-ttu-id="917b6-108">Funciones de cliente DRM de Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="917b6-108">Microsoft Windows Media DRM Client Functions</span></span>

<span data-ttu-id="917b6-109">Las siguientes funciones se implementan como parte de las API extendidas del cliente DRM de Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="917b6-109">The following functions are implemented as part of the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="917b6-110">Función</span><span class="sxs-lookup"><span data-stu-id="917b6-110">Function</span></span>                                                             | <span data-ttu-id="917b6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="917b6-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="917b6-112">**WMDRMCreateProvider**</span><span class="sxs-lookup"><span data-stu-id="917b6-112">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)                   | <span data-ttu-id="917b6-113">Crea un generador de clases que puede crear los demás objetos DRM.</span><span class="sxs-lookup"><span data-stu-id="917b6-113">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="917b6-114">Esta función no requiere una biblioteca de código auxiliar de Microsoft y crea objetos que no admiten las características DRM protegidas.</span><span class="sxs-lookup"><span data-stu-id="917b6-114">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span> |
| [<span data-ttu-id="917b6-115">**WMDRMCreateProtectedProvider**</span><span class="sxs-lookup"><span data-stu-id="917b6-115">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md) | <span data-ttu-id="917b6-116">Crea un generador de clases que puede crear los demás objetos DRM.</span><span class="sxs-lookup"><span data-stu-id="917b6-116">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="917b6-117">Esta función requiere una biblioteca de código auxiliar de Microsoft y crea objetos que admiten las características DRM protegidas.</span><span class="sxs-lookup"><span data-stu-id="917b6-117">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>                |
| [<span data-ttu-id="917b6-118">**WMDRMShutdown**</span><span class="sxs-lookup"><span data-stu-id="917b6-118">**WMDRMShutdown**</span></span>](wmdrmshutdown.md)                               | <span data-ttu-id="917b6-119">Libera los recursos utilizados por las API.</span><span class="sxs-lookup"><span data-stu-id="917b6-119">Releases resources used by the APIs.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="917b6-120">**WMDRMStartup**</span><span class="sxs-lookup"><span data-stu-id="917b6-120">**WMDRMStartup**</span></span>](wmdrmstartup.md)                                 | <span data-ttu-id="917b6-121">Inicializa los recursos utilizados por las API.</span><span class="sxs-lookup"><span data-stu-id="917b6-121">Initializes resources used by the APIs.</span></span>                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="917b6-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="917b6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="917b6-123">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="917b6-123">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




