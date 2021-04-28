---
description: 'Métodos virtuales puros de CMSPCallBase: estas clases derivadas deben invalidar estos métodos.'
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Métodos virtuales puros de CMSPCallBase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094463"
---
# <a name="cmspcallbase-pure-virtual-methods"></a><span data-ttu-id="71ea2-103">Métodos virtuales puros de CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="71ea2-103">CMSPCallBase Pure Virtual Methods</span></span>

<span data-ttu-id="71ea2-104">Estas clases derivadas deben invalidar estos métodos.</span><span class="sxs-lookup"><span data-stu-id="71ea2-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="71ea2-105">Métodos virtuales puros de CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="71ea2-105">CMSPCallBase pure virtual methods</span></span>                                 | <span data-ttu-id="71ea2-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="71ea2-106">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="71ea2-107">**MSPCallAddRef**</span><span class="sxs-lookup"><span data-stu-id="71ea2-107">**MSPCallAddRef**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | <span data-ttu-id="71ea2-108">Método AddRef privado para el objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="71ea2-108">Private AddRef method for the call object.</span></span>                                                                                              |
| [<span data-ttu-id="71ea2-109">**MSPCallRelease**</span><span class="sxs-lookup"><span data-stu-id="71ea2-109">**MSPCallRelease**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | <span data-ttu-id="71ea2-110">Método Private Release para el objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="71ea2-110">Private Release method for the call object.</span></span>                                                                                             |
| [<span data-ttu-id="71ea2-111">**Init**</span><span class="sxs-lookup"><span data-stu-id="71ea2-111">**Init**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | <span data-ttu-id="71ea2-112">Llamado por el objeto de dirección MSP (en el [**método CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) para inicializar el objeto de llamada MSP.</span><span class="sxs-lookup"><span data-stu-id="71ea2-112">Called by the MSP address object (in the method [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) to initialize the MSP call object.</span></span> |
| [<span data-ttu-id="71ea2-113">**Apagado**</span><span class="sxs-lookup"><span data-stu-id="71ea2-113">**ShutDown**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | <span data-ttu-id="71ea2-114">Llamado por el objeto de dirección MSP para apagar la llamada.</span><span class="sxs-lookup"><span data-stu-id="71ea2-114">Called by the MSP address object to shut down the call..</span></span>                                                                                |
| [<span data-ttu-id="71ea2-115">**InternalCreateStream**</span><span class="sxs-lookup"><span data-stu-id="71ea2-115">**InternalCreateStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | <span data-ttu-id="71ea2-116">Lo llama [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) para crear un objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="71ea2-116">Called by [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) to create a stream object.</span></span>                                               |
| [<span data-ttu-id="71ea2-117">**CreateStreamObject**</span><span class="sxs-lookup"><span data-stu-id="71ea2-117">**CreateStreamObject**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | <span data-ttu-id="71ea2-118">[**InternalCreateStream llama a para**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) crear un objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="71ea2-118">Called by [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) to create a stream object.</span></span>                                  |
| [<span data-ttu-id="71ea2-119">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="71ea2-119">**RemoveStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | <span data-ttu-id="71ea2-120">Llamado por la aplicación para quitar una secuencia de la llamada</span><span class="sxs-lookup"><span data-stu-id="71ea2-120">Called by the application to remove a stream from the call</span></span>                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="71ea2-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71ea2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71ea2-122">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="71ea2-122">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
