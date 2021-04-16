---
title: Atributo DLNAServerUDN
description: El atributo DLNAServerUDN es el nombre de dispositivo único del servidor que hospeda el elemento multimedia.
ms.assetid: 1965731d-1b6e-4d76-a983-fd57c851fcfb
keywords:
- DLNAServerUDN Media Player de Windows
topic_type:
- apiref
api_name:
- DLNAServerUDN Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caa121df7a4f312e3cb00519d2ac4f519f844d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699887"
---
# <a name="dlnaserverudn-attribute"></a><span data-ttu-id="7f69f-104">Atributo DLNAServerUDN</span><span class="sxs-lookup"><span data-stu-id="7f69f-104">DLNAServerUDN Attribute</span></span>

<span data-ttu-id="7f69f-105">El atributo **DLNAServerUDN** es el nombre de dispositivo único del servidor que hospeda el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="7f69f-105">The **DLNAServerUDN** attribute is the unique device name of the server that hosts the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="7f69f-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="7f69f-106">Applies To</span></span>

-   [<span data-ttu-id="7f69f-107">**Elementos de audio**</span><span class="sxs-lookup"><span data-stu-id="7f69f-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="7f69f-108">**Elementos de fotografía**</span><span class="sxs-lookup"><span data-stu-id="7f69f-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="7f69f-109">**Elementos de lista de reproducción**</span><span class="sxs-lookup"><span data-stu-id="7f69f-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="7f69f-110">**Elementos de vídeo**</span><span class="sxs-lookup"><span data-stu-id="7f69f-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="7f69f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f69f-111">Remarks</span></span>

<span data-ttu-id="7f69f-112">Este atributo no está disponible para los elementos multimedia de la biblioteca local del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="7f69f-112">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="7f69f-113">Solo está disponible para los elementos multimedia que pertenecen a una biblioteca remota. es decir, una biblioteca que otro usuario ha puesto a disposición en la red doméstica.</span><span class="sxs-lookup"><span data-stu-id="7f69f-113">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="7f69f-114">Para determinar si una biblioteca multimedia es remota, llame a [**IWMPLibrary:: get \_ Type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="7f69f-114">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f69f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f69f-115">Requirements</span></span>



| <span data-ttu-id="7f69f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f69f-116">Requirement</span></span> | <span data-ttu-id="7f69f-117">Value</span><span class="sxs-lookup"><span data-stu-id="7f69f-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="7f69f-118">Versión</span><span class="sxs-lookup"><span data-stu-id="7f69f-118">Version</span></span><br/> | <span data-ttu-id="7f69f-119">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="7f69f-119">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f69f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f69f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f69f-121">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="7f69f-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





