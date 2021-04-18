---
title: Atributo AlbumID
description: El atributo AlbumID es un identificador único para el álbum.
ms.assetid: 0412d91a-11a7-434c-8717-a71d85655679
keywords:
- AlbumID Media Player de Windows
topic_type:
- apiref
api_name:
- AlbumID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339253c82554579fa549371e2ebe4cb2f1926cc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700395"
---
# <a name="albumid-attribute"></a><span data-ttu-id="9c99a-104">Atributo AlbumID</span><span class="sxs-lookup"><span data-stu-id="9c99a-104">AlbumID Attribute</span></span>

<span data-ttu-id="9c99a-105">El atributo **albumid** es un identificador único para el álbum.</span><span class="sxs-lookup"><span data-stu-id="9c99a-105">The **AlbumID** attribute is a unique identifier for the album.</span></span>

## <a name="applies-to"></a><span data-ttu-id="9c99a-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="9c99a-106">Applies To</span></span>

-   [<span data-ttu-id="9c99a-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="9c99a-107">Audio Items</span></span>](audio-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="9c99a-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c99a-108">Remarks</span></span>

<span data-ttu-id="9c99a-109">Este atributo solo se almacena en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="9c99a-109">This attribute is stored only in the library.</span></span>

<span data-ttu-id="9c99a-110">El identificador único es una combinación del título del álbum y el nombre del intérprete del álbum.</span><span class="sxs-lookup"><span data-stu-id="9c99a-110">The unique identifier is a combination of the album title and the album artist name.</span></span> <span data-ttu-id="9c99a-111">En este atributo, el título del álbum aparece primero.</span><span class="sxs-lookup"><span data-stu-id="9c99a-111">In this attribute, the album title comes first.</span></span> <span data-ttu-id="9c99a-112">Cuando se usa el método [MediaCollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) para obtener un objeto **StringCollection** mediante este atributo, los valores se ordenan por título del álbum.</span><span class="sxs-lookup"><span data-stu-id="9c99a-112">When you use the [MediaCollection.getAttributeStringCollection](mediacollection-getattributestringcollection.md) method to get a **StringCollection** object using this attribute, the values are sorted by album title.</span></span>

<span data-ttu-id="9c99a-113">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="9c99a-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c99a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c99a-114">Requirements</span></span>



| <span data-ttu-id="9c99a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c99a-115">Requirement</span></span> | <span data-ttu-id="9c99a-116">Value</span><span class="sxs-lookup"><span data-stu-id="9c99a-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="9c99a-117">Versión</span><span class="sxs-lookup"><span data-stu-id="9c99a-117">Version</span></span><br/> | <span data-ttu-id="9c99a-118">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="9c99a-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c99a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c99a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c99a-120">**Atributo AlbumIDAlbumArtist**</span><span class="sxs-lookup"><span data-stu-id="9c99a-120">**AlbumIDAlbumArtist Attribute**</span></span>](albumidalbumartist-attribute.md)
</dt> <dt>

[<span data-ttu-id="9c99a-121">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="9c99a-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





