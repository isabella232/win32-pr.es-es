---
title: Atributo CDTrackEnabled
description: El atributo CDTrackEnabled indica si la pista está habilitada para la reproducción.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- CDTrackEnabled Media Player de Windows
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700308"
---
# <a name="cdtrackenabled-attribute"></a><span data-ttu-id="e03b2-104">Atributo CDTrackEnabled</span><span class="sxs-lookup"><span data-stu-id="e03b2-104">CDTrackEnabled Attribute</span></span>

<span data-ttu-id="e03b2-105">El atributo **CDTrackEnabled** indica si la pista está habilitada para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="e03b2-105">The **CDTrackEnabled** attribute indicates whether the track is enabled for playback.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e03b2-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="e03b2-106">Applies To</span></span>

-   [<span data-ttu-id="e03b2-107">Pistas de CD</span><span class="sxs-lookup"><span data-stu-id="e03b2-107">CD Tracks</span></span>](cd-track-attributes.md)

## <a name="remarks"></a><span data-ttu-id="e03b2-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e03b2-108">Remarks</span></span>

<span data-ttu-id="e03b2-109">Este atributo solo se almacena en la memoria caché de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e03b2-109">This attribute is stored only in the library cache.</span></span>

<span data-ttu-id="e03b2-110">Al reproducir un CD en Windows Media Player, el usuario puede seleccionar una pista y especificar que no se debe reproducir.</span><span class="sxs-lookup"><span data-stu-id="e03b2-110">When playing a CD in Windows Media Player, the user may select a track and specify that it should not be played.</span></span> <span data-ttu-id="e03b2-111">Este valor de este atributo es true si se puede reproducir la pista o false si el usuario especificó que no se debe reproducir la pista.</span><span class="sxs-lookup"><span data-stu-id="e03b2-111">This value of this attribute is True if the track can be played, or False if the user specified that the track should not be played.</span></span>

<span data-ttu-id="e03b2-112">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="e03b2-112">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e03b2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e03b2-113">Requirements</span></span>



| <span data-ttu-id="e03b2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e03b2-114">Requirement</span></span> | <span data-ttu-id="e03b2-115">Value</span><span class="sxs-lookup"><span data-stu-id="e03b2-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="e03b2-116">Versión</span><span class="sxs-lookup"><span data-stu-id="e03b2-116">Version</span></span><br/> | <span data-ttu-id="e03b2-117">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="e03b2-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e03b2-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e03b2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e03b2-119">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="e03b2-119">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





