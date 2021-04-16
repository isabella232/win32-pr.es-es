---
title: Atributo DisplayArtist
description: El atributo DisplayArtist es el nombre del artista que se muestra para un elemento.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- DisplayArtist Media Player de Windows
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699624"
---
# <a name="displayartist-attribute"></a><span data-ttu-id="f03c7-104">Atributo DisplayArtist</span><span class="sxs-lookup"><span data-stu-id="f03c7-104">DisplayArtist Attribute</span></span>

<span data-ttu-id="f03c7-105">El atributo **DisplayArtist** es el nombre del artista que se muestra para un elemento.</span><span class="sxs-lookup"><span data-stu-id="f03c7-105">The **DisplayArtist** attribute is the name of the artist that is displayed for an item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f03c7-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="f03c7-106">Applies To</span></span>

-   [<span data-ttu-id="f03c7-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="f03c7-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="f03c7-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f03c7-108">Remarks</span></span>

<span data-ttu-id="f03c7-109">Por lo general, **DisplayArtist** tendrá el mismo valor que el atributo **WM/AlbumArtist** cuando se establezca ese atributo.</span><span class="sxs-lookup"><span data-stu-id="f03c7-109">Generally, **DisplayArtist** will have the same value as the **WM/AlbumArtist** attribute when that attribute is set.</span></span> <span data-ttu-id="f03c7-110">De lo contrario, el valor será el nombre del artista asociado a la primera pista del álbum.</span><span class="sxs-lookup"><span data-stu-id="f03c7-110">Otherwise, the value will be the name of the artist that is associated with the first track on the album.</span></span>

<span data-ttu-id="f03c7-111">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="f03c7-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f03c7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f03c7-112">Requirements</span></span>



| <span data-ttu-id="f03c7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f03c7-113">Requirement</span></span> | <span data-ttu-id="f03c7-114">Value</span><span class="sxs-lookup"><span data-stu-id="f03c7-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="f03c7-115">Versión</span><span class="sxs-lookup"><span data-stu-id="f03c7-115">Version</span></span><br/> | <span data-ttu-id="f03c7-116">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="f03c7-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f03c7-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="f03c7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f03c7-118">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="f03c7-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="f03c7-119">**Atributo WM/AlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="f03c7-119">**WM/AlbumArtist Attribute**</span></span>](wm-albumartist-attribute.md)
</dt> </dl>

 

 





