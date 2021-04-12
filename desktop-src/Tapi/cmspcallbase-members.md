---
description: La lista siguiente contiene los miembros de CMSPCAllBase.
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: Miembros de CMSPCallBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276990"
---
# <a name="cmspcallbase-members"></a><span data-ttu-id="dcf65-103">Miembros de CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="dcf65-103">CMSPCallBase Members</span></span>



| <span data-ttu-id="dcf65-104">Tipo de miembro</span><span class="sxs-lookup"><span data-stu-id="dcf65-104">Member type</span></span>                   | <span data-ttu-id="dcf65-105">Nombre</span><span class="sxs-lookup"><span data-stu-id="dcf65-105">Name</span></span>             | <span data-ttu-id="dcf65-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcf65-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf65-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="dcf65-107">IUnknown</span></span>                      | <span data-ttu-id="dcf65-108">\*m \_ pFTM</span><span class="sxs-lookup"><span data-stu-id="dcf65-108">\*m\_pFTM</span></span>        | <span data-ttu-id="dcf65-109">Puntero al serializador de subprocesamiento libre.</span><span class="sxs-lookup"><span data-stu-id="dcf65-109">Pointer to the free threaded marshaller.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="dcf65-110">CMSPAddress\*</span><span class="sxs-lookup"><span data-stu-id="dcf65-110">CMSPAddress\*</span></span>                 | <span data-ttu-id="dcf65-111">\*m \_ pMSPAddress</span><span class="sxs-lookup"><span data-stu-id="dcf65-111">\*m\_pMSPAddress</span></span> | <span data-ttu-id="dcf65-112">Puntero al objeto de dirección MSP.</span><span class="sxs-lookup"><span data-stu-id="dcf65-112">The pointer to the MSP address object.</span></span> <span data-ttu-id="dcf65-113">Se usa para obtener los terminales predeterminados si la aplicación no selecciona ninguno.</span><span class="sxs-lookup"><span data-stu-id="dcf65-113">It is used to get the default terminals if the application doesn't select any.</span></span> <span data-ttu-id="dcf65-114">También incluye un refcount (a través de [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), no AddRef), por lo que la dirección agregada no desaparecerá mientras la llamada está todavía activa, pero la dirección de TAPI 3 no es AddRef'ed.</span><span class="sxs-lookup"><span data-stu-id="dcf65-114">It also carries a refcount (via [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), not AddRef) so that the aggregated address will not go away while the call is still alive, but TAPI 3's address is not AddRef'ed.</span></span> |
| <span data-ttu-id="dcf65-115">identificador de MSP \_</span><span class="sxs-lookup"><span data-stu-id="dcf65-115">MSP\_HANDLE</span></span>                   | <span data-ttu-id="dcf65-116">\*m \_ htCall</span><span class="sxs-lookup"><span data-stu-id="dcf65-116">\*m\_htCall</span></span>      | <span data-ttu-id="dcf65-117">Identificador de la llamada a TAPI3's.</span><span class="sxs-lookup"><span data-stu-id="dcf65-117">The handle to TAPI3's call.</span></span> <span data-ttu-id="dcf65-118">Se usa para desencadenar eventos de llamada.</span><span class="sxs-lookup"><span data-stu-id="dcf65-118">Used to fire call events.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="dcf65-119">DWORD</span><span class="sxs-lookup"><span data-stu-id="dcf65-119">DWORD</span></span>                         | <span data-ttu-id="dcf65-120">m \_ dwMediaType</span><span class="sxs-lookup"><span data-stu-id="dcf65-120">m\_dwMediaType</span></span>   | <span data-ttu-id="dcf65-121">Máscara de archivo de los tipos de medios en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="dcf65-121">Bitmask of the media types on this call.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="dcf65-122">CMSPArray <ITStream \*></span><span class="sxs-lookup"><span data-stu-id="dcf65-122">CMSPArray <ITStream \*></span></span> | <span data-ttu-id="dcf65-123">\_flujos m</span><span class="sxs-lookup"><span data-stu-id="dcf65-123">m\_Streams</span></span>       | <span data-ttu-id="dcf65-124">Lista de objetos de secuencia de la llamada.</span><span class="sxs-lookup"><span data-stu-id="dcf65-124">The list of stream objects in the call.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="dcf65-125">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="dcf65-125">CMSPCritSection</span></span>               | <span data-ttu-id="dcf65-126">\_bloqueo m</span><span class="sxs-lookup"><span data-stu-id="dcf65-126">m\_lock</span></span>          | <span data-ttu-id="dcf65-127">El bloqueo que protege las listas de secuencias.</span><span class="sxs-lookup"><span data-stu-id="dcf65-127">The lock that protects the stream lists.</span></span>                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="dcf65-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dcf65-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcf65-129">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="dcf65-129">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



