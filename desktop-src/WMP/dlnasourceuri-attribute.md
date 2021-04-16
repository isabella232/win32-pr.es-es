---
title: Atributo DLNASourceURI
description: El atributo DLNASourceURI es el identificador de recursos universal (URI) del elemento.
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- DLNASourceURI Media Player de Windows
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699580"
---
# <a name="dlnasourceuri-attribute"></a><span data-ttu-id="b3010-104">Atributo DLNASourceURI</span><span class="sxs-lookup"><span data-stu-id="b3010-104">DLNASourceURI Attribute</span></span>

<span data-ttu-id="b3010-105">El atributo **DLNASourceURI** es el identificador de recursos universal (URI) del elemento.</span><span class="sxs-lookup"><span data-stu-id="b3010-105">The **DLNASourceURI** attribute is the universal resource identifier (URI) of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b3010-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="b3010-106">Applies To</span></span>

-   [<span data-ttu-id="b3010-107">**Elementos de audio**</span><span class="sxs-lookup"><span data-stu-id="b3010-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="b3010-108">**Otros elementos**</span><span class="sxs-lookup"><span data-stu-id="b3010-108">**Other Items**</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="b3010-109">**Elementos de fotografía**</span><span class="sxs-lookup"><span data-stu-id="b3010-109">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="b3010-110">**Elementos de lista de reproducción**</span><span class="sxs-lookup"><span data-stu-id="b3010-110">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="b3010-111">**Elementos de vídeo**</span><span class="sxs-lookup"><span data-stu-id="b3010-111">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b3010-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3010-112">Remarks</span></span>

<span data-ttu-id="b3010-113">Si el elemento se encuentra en la biblioteca local del usuario actual, este atributo, el atributo [**SourceURL**](sourceurl-attribute.md) y el valor devuelto por [**IWMPMedia:: get \_ SourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) son los mismos.</span><span class="sxs-lookup"><span data-stu-id="b3010-113">If the item is in the current user's local library, this attribute, the [**SourceURL**](sourceurl-attribute.md) attribute, and the value returned by [**IWMPMedia::get\_sourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) are all the same.</span></span>

<span data-ttu-id="b3010-114">Si el elemento no está en la biblioteca local del usuario actual, pero pertenece a una biblioteca remota, este atributo es un identificador con el formato DLNA-playsingle://*XXX*.</span><span class="sxs-lookup"><span data-stu-id="b3010-114">If the item is not in the current user's local library, but belongs to a remote library, this attribute is an identifier of the form dlna-playsingle://*xxx*.</span></span>

<span data-ttu-id="b3010-115">Puede pasar un URI DLNA-playsingle al método [**IWMPCore3:: newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) para obtener una interfaz [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) que le permita ver los metadatos del elemento multimedia y modificar potencialmente la clasificación de estrellas del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="b3010-115">You can pass a dlna-playsingle URI to the [**IWMPCore3::newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) method to obtain an [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) interface that enables you to view the media item's metadata and potentially edit the media item's star rating.</span></span> <span data-ttu-id="b3010-116">Sin embargo, tenga en cuenta que el URI DLNA-playsingle debe ser para un servicio de directorio de contenido (CDS) que Windows Media Player ya haya detectado.</span><span class="sxs-lookup"><span data-stu-id="b3010-116">Note, however, that the dlna-playsingle URI must be for a content directory service (CDS) that Windows Media Player has already discovered.</span></span> <span data-ttu-id="b3010-117">El método **newMedia** no iniciará la detección de UPnP y buscará los CD.</span><span class="sxs-lookup"><span data-stu-id="b3010-117">The **newMedia** method will not initiate UPnP discovery and search for the CDS.</span></span>

<span data-ttu-id="b3010-118">Solo puede editar la clasificación por estrellas de un elemento multimedia en una biblioteca remota si la biblioteca remota admite la operación de edición.</span><span class="sxs-lookup"><span data-stu-id="b3010-118">You can edit the star rating of a media item in a remote library only if the remote library supports the edit operation.</span></span> <span data-ttu-id="b3010-119">Las bibliotecas remotas hospedadas en un equipo que ejecuta Windows 7 admiten la operación de edición.</span><span class="sxs-lookup"><span data-stu-id="b3010-119">Remote libraries hosted on a computer running Windows 7 support the edit operation.</span></span> <span data-ttu-id="b3010-120">Las bibliotecas remotas hospedadas en un equipo que ejecuta un sistema operativo Windows anterior a Windows 7 no admiten la operación de edición.</span><span class="sxs-lookup"><span data-stu-id="b3010-120">Remote libraries hosted on a computer running a Windows operating system earlier than Windows 7 do not support the edit operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3010-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3010-121">Requirements</span></span>



| <span data-ttu-id="b3010-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3010-122">Requirement</span></span> | <span data-ttu-id="b3010-123">Value</span><span class="sxs-lookup"><span data-stu-id="b3010-123">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="b3010-124">Versión</span><span class="sxs-lookup"><span data-stu-id="b3010-124">Version</span></span><br/> | <span data-ttu-id="b3010-125">Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="b3010-125">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3010-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3010-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3010-127">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="b3010-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





