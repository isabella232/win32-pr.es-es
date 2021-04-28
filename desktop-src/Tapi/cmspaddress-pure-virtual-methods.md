---
description: 'CmSPAddress Pure Virtual Methods : estas clases derivadas deben reemplazar estos métodos.'
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Métodos virtuales puros de CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d9b9494e4ee42972d97433927fd587034af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084213"
---
# <a name="cmspaddress-pure-virtual-methods"></a><span data-ttu-id="c870e-103">Métodos virtuales puros de CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="c870e-103">CMSPAddress Pure Virtual Methods</span></span>

<span data-ttu-id="c870e-104">Estos métodos deben reemplazarse por clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="c870e-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="c870e-105">Métodos virtuales puros de CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="c870e-105">CMSPAddress pure virtual methods</span></span>                           | <span data-ttu-id="c870e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c870e-106">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c870e-107">**MSPAddressAddRef**</span><span class="sxs-lookup"><span data-stu-id="c870e-107">**MSPAddressAddRef**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | <span data-ttu-id="c870e-108">Método AddRef privado para la dirección.</span><span class="sxs-lookup"><span data-stu-id="c870e-108">Private AddRef method for the address.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="c870e-109">**MSPAddressRelease**</span><span class="sxs-lookup"><span data-stu-id="c870e-109">**MSPAddressRelease**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | <span data-ttu-id="c870e-110">Método Private Release para la dirección.</span><span class="sxs-lookup"><span data-stu-id="c870e-110">Private Release method for the address.</span></span>                                                                                                                                                |
| [<span data-ttu-id="c870e-111">**CreateMSPCall**</span><span class="sxs-lookup"><span data-stu-id="c870e-111">**CreateMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | <span data-ttu-id="c870e-112">TapI llama a para crear un objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="c870e-112">Called by TAPI to create a call object.</span></span> <span data-ttu-id="c870e-113">La implementación de la clase derivada simplemente debe llamar a la [**función CreateMSPCallHelper.**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper)</span><span class="sxs-lookup"><span data-stu-id="c870e-113">The implementation in the derived class should simply call the [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) function.</span></span>        |
| [<span data-ttu-id="c870e-114">**ShutdownMSPCall**</span><span class="sxs-lookup"><span data-stu-id="c870e-114">**ShutdownMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | <span data-ttu-id="c870e-115">Lo llama TAPI para apagar un objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="c870e-115">Called by TAPI to shut down a call object.</span></span> <span data-ttu-id="c870e-116">La implementación de la clase derivada simplemente debe llamar a la [**función ShutdownMSPCallHelper.**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper)</span><span class="sxs-lookup"><span data-stu-id="c870e-116">The implementation in the derived class should simply call the [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) function.</span></span> |
| [<span data-ttu-id="c870e-117">**GetCallMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="c870e-117">**GetCallMediaTypes**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | <span data-ttu-id="c870e-118">Obtiene los tipos de medios admitidos por el MSP.</span><span class="sxs-lookup"><span data-stu-id="c870e-118">Gets media types supported by the MSP.</span></span>                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="c870e-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c870e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c870e-120">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="c870e-120">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



