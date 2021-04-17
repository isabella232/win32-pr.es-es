---
title: Atributo AlbumIDAlbumArtist
description: El atributo AlbumIDAlbumArtist es un identificador único para el álbum.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- AlbumIDAlbumArtist Media Player de Windows
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1925f40a50b15efcd339ad949d5d54ddb915cbe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700077"
---
# <a name="albumidalbumartist-attribute"></a><span data-ttu-id="9235d-104">Atributo AlbumIDAlbumArtist</span><span class="sxs-lookup"><span data-stu-id="9235d-104">AlbumIDAlbumArtist Attribute</span></span>

<span data-ttu-id="9235d-105">El atributo **AlbumIDAlbumArtist** es un identificador único para el álbum.</span><span class="sxs-lookup"><span data-stu-id="9235d-105">The **AlbumIDAlbumArtist** attribute is a unique identifier for the album.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9235d-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="9235d-106">Applies To</span></span>

-   [<span data-ttu-id="9235d-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="9235d-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="9235d-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9235d-108">Remarks</span></span>

<span data-ttu-id="9235d-109">Este atributo solo se almacena en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9235d-109">This attribute is stored only in the library.</span></span>

<span data-ttu-id="9235d-110">El identificador único es una combinación del título del álbum y el nombre del intérprete del álbum.</span><span class="sxs-lookup"><span data-stu-id="9235d-110">The unique identifier is a combination of the album title and the album artist name.</span></span> <span data-ttu-id="9235d-111">En este atributo, el nombre del intérprete del álbum aparece primero.</span><span class="sxs-lookup"><span data-stu-id="9235d-111">In this attribute, the album artist name comes first.</span></span> <span data-ttu-id="9235d-112">Cuando se usa el método [MediaCollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) para obtener un objeto **StringCollection** mediante este atributo, los valores se ordenan por nombre de intérprete del álbum.</span><span class="sxs-lookup"><span data-stu-id="9235d-112">When you use the [MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) method to get a **StringCollection** object using this attribute, the values are sorted by album artist name.</span></span>

<span data-ttu-id="9235d-113">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="9235d-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9235d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9235d-114">Requirements</span></span>



| <span data-ttu-id="9235d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9235d-115">Requirement</span></span> | <span data-ttu-id="9235d-116">Value</span><span class="sxs-lookup"><span data-stu-id="9235d-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="9235d-117">Versión</span><span class="sxs-lookup"><span data-stu-id="9235d-117">Version</span></span><br/> | <span data-ttu-id="9235d-118">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="9235d-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9235d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9235d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9235d-120">**Atributo AlbumID**</span><span class="sxs-lookup"><span data-stu-id="9235d-120">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="9235d-121">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="9235d-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





