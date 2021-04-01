---
description: Estos métodos deben reemplazarse por clases derivadas.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Métodos virtuales puros de CMSPCallBase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d8dea4c1a240e362a4dc3a19b3c09a37a318947
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103909997"
---
# <a name="cmspcallbase-pure-virtual-methods"></a><span data-ttu-id="044e6-103">Métodos virtuales puros de CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="044e6-103">CMSPCallBase Pure Virtual Methods</span></span>

<span data-ttu-id="044e6-104">Estos métodos deben reemplazarse por clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="044e6-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="044e6-105">Métodos virtuales puros de CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="044e6-105">CMSPCallBase pure virtual methods</span></span>                                 | <span data-ttu-id="044e6-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="044e6-106">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="044e6-107">**MSPCallAddRef**</span><span class="sxs-lookup"><span data-stu-id="044e6-107">**MSPCallAddRef**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | <span data-ttu-id="044e6-108">Método AddRef privado para el objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="044e6-108">Private AddRef method for the call object.</span></span>                                                                                              |
| [<span data-ttu-id="044e6-109">**MSPCallRelease**</span><span class="sxs-lookup"><span data-stu-id="044e6-109">**MSPCallRelease**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | <span data-ttu-id="044e6-110">Método de liberación privado para el objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="044e6-110">Private Release method for the call object.</span></span>                                                                                             |
| [<span data-ttu-id="044e6-111">**Smss**</span><span class="sxs-lookup"><span data-stu-id="044e6-111">**Init**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | <span data-ttu-id="044e6-112">Lo llama el objeto de dirección MSP (en el método [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) para inicializar el objeto de llamada MSP.</span><span class="sxs-lookup"><span data-stu-id="044e6-112">Called by the MSP address object (in the method [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) to initialize the MSP call object.</span></span> |
| [<span data-ttu-id="044e6-113">**Apagado**</span><span class="sxs-lookup"><span data-stu-id="044e6-113">**ShutDown**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | <span data-ttu-id="044e6-114">Lo llama el objeto de dirección MSP para cerrar la llamada.</span><span class="sxs-lookup"><span data-stu-id="044e6-114">Called by the MSP address object to shut down the call..</span></span>                                                                                |
| [<span data-ttu-id="044e6-115">**InternalCreateStream**</span><span class="sxs-lookup"><span data-stu-id="044e6-115">**InternalCreateStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | <span data-ttu-id="044e6-116">Llamado por [**CreateStream (**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) para crear un objeto de flujo.</span><span class="sxs-lookup"><span data-stu-id="044e6-116">Called by [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) to create a stream object.</span></span>                                               |
| [<span data-ttu-id="044e6-117">**CreateStreamObject**</span><span class="sxs-lookup"><span data-stu-id="044e6-117">**CreateStreamObject**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | <span data-ttu-id="044e6-118">Llamado por [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) para crear un objeto de flujo.</span><span class="sxs-lookup"><span data-stu-id="044e6-118">Called by [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) to create a stream object.</span></span>                                  |
| [<span data-ttu-id="044e6-119">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="044e6-119">**RemoveStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | <span data-ttu-id="044e6-120">La aplicación llama a este método para quitar un flujo de la llamada.</span><span class="sxs-lookup"><span data-stu-id="044e6-120">Called by the application to remove a stream from the call</span></span>                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="044e6-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="044e6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="044e6-122">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="044e6-122">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
