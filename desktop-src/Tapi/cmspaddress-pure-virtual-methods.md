---
description: Estos métodos deben reemplazarse por clases derivadas.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Métodos virtuales puros de CMSPAddress
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687566"
---
# <a name="cmspaddress-pure-virtual-methods"></a><span data-ttu-id="d4383-103">Métodos virtuales puros de CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="d4383-103">CMSPAddress Pure Virtual Methods</span></span>

<span data-ttu-id="d4383-104">Estos métodos deben reemplazarse por clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="d4383-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="d4383-105">Métodos virtuales puros de CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="d4383-105">CMSPAddress pure virtual methods</span></span>                           | <span data-ttu-id="d4383-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4383-106">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4383-107">**MSPAddressAddRef**</span><span class="sxs-lookup"><span data-stu-id="d4383-107">**MSPAddressAddRef**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | <span data-ttu-id="d4383-108">Método AddRef privado para la dirección.</span><span class="sxs-lookup"><span data-stu-id="d4383-108">Private AddRef method for the address.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="d4383-109">**MSPAddressRelease**</span><span class="sxs-lookup"><span data-stu-id="d4383-109">**MSPAddressRelease**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | <span data-ttu-id="d4383-110">Método de versión privada para la dirección.</span><span class="sxs-lookup"><span data-stu-id="d4383-110">Private Release method for the address.</span></span>                                                                                                                                                |
| [<span data-ttu-id="d4383-111">**CreateMSPCall**</span><span class="sxs-lookup"><span data-stu-id="d4383-111">**CreateMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | <span data-ttu-id="d4383-112">Lo llama TAPI para crear un objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="d4383-112">Called by TAPI to create a call object.</span></span> <span data-ttu-id="d4383-113">La implementación en la clase derivada debe llamar simplemente a la función [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) .</span><span class="sxs-lookup"><span data-stu-id="d4383-113">The implementation in the derived class should simply call the [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) function.</span></span>        |
| [<span data-ttu-id="d4383-114">**ShutdownMSPCall**</span><span class="sxs-lookup"><span data-stu-id="d4383-114">**ShutdownMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | <span data-ttu-id="d4383-115">Lo llama TAPI para cerrar un objeto de llamada.</span><span class="sxs-lookup"><span data-stu-id="d4383-115">Called by TAPI to shut down a call object.</span></span> <span data-ttu-id="d4383-116">La implementación en la clase derivada debe llamar simplemente a la función [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) .</span><span class="sxs-lookup"><span data-stu-id="d4383-116">The implementation in the derived class should simply call the [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) function.</span></span> |
| [<span data-ttu-id="d4383-117">**GetCallMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="d4383-117">**GetCallMediaTypes**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | <span data-ttu-id="d4383-118">Obtiene los tipos de medios admitidos por MSP.</span><span class="sxs-lookup"><span data-stu-id="d4383-118">Gets media types supported by the MSP.</span></span>                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="d4383-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4383-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4383-120">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="d4383-120">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



