---
title: Atributo DTCPIPHost
description: El atributo DTCPIPHost es el nombre o la dirección IP del equipo o dispositivo en el que se debe establecer contacto para la transmisión digital Content Protection a través del Protocolo de Internet (DTCP-IP) intercambio de claves autenticado (Rear) para el elemento multimedia.
ms.assetid: 61b7d6fb-c216-49ae-811a-8ce42fdb71e4
keywords:
- DTCPIPHost Media Player de Windows
topic_type:
- apiref
api_name:
- DTCPIPHost Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9983cac920f2d11b9040e03af30e10b9c0c3fbcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700033"
---
# <a name="dtcpiphost-attribute"></a><span data-ttu-id="e8246-104">Atributo DTCPIPHost</span><span class="sxs-lookup"><span data-stu-id="e8246-104">DTCPIPHost Attribute</span></span>

<span data-ttu-id="e8246-105">El atributo **DTCPIPHost** es el nombre o la dirección IP del equipo o dispositivo en el que se debe establecer contacto para la transmisión digital Content Protection a través del Protocolo de Internet (DTCP-IP) intercambio de claves autenticado (Rear) para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="e8246-105">The **DTCPIPHost** attribute is the name or IP address of the computer or device that must be contacted for the Digital Transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) for the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e8246-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="e8246-106">Applies To</span></span>

-   [<span data-ttu-id="e8246-107">**Elementos de audio**</span><span class="sxs-lookup"><span data-stu-id="e8246-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="e8246-108">**Elementos de fotografía**</span><span class="sxs-lookup"><span data-stu-id="e8246-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="e8246-109">**Elementos de lista de reproducción**</span><span class="sxs-lookup"><span data-stu-id="e8246-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="e8246-110">**Elementos de vídeo**</span><span class="sxs-lookup"><span data-stu-id="e8246-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="e8246-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8246-111">Remarks</span></span>

<span data-ttu-id="e8246-112">Si este atributo está disponible, el elemento multimedia se protege mediante DTCP-IP.</span><span class="sxs-lookup"><span data-stu-id="e8246-112">If this attribute is available, the media item is protected using DTCP-IP.</span></span>

<span data-ttu-id="e8246-113">Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="e8246-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="e8246-114">Solo está disponible para los elementos multimedia que pertenecen a una biblioteca remota. es decir, una biblioteca que otro usuario ha puesto a disposición en la red doméstica.</span><span class="sxs-lookup"><span data-stu-id="e8246-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="e8246-115">Para determinar si una biblioteca multimedia es remota, llame a [**IWMPLibrary:: get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="e8246-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8246-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8246-116">Requirements</span></span>



| <span data-ttu-id="e8246-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8246-117">Requirement</span></span> | <span data-ttu-id="e8246-118">Value</span><span class="sxs-lookup"><span data-stu-id="e8246-118">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="e8246-119">Versión</span><span class="sxs-lookup"><span data-stu-id="e8246-119">Version</span></span><br/> | <span data-ttu-id="e8246-120">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="e8246-120">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8246-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8246-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8246-122">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="e8246-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





