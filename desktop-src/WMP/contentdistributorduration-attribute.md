---
title: Atributo ContentDistributorDuration
description: El atributo ContentDistributorDuration es la duración de la reproducción del elemento, en segundos.
ms.assetid: c64cb4ca-b0bc-4beb-b2ae-ddd0c5fcd35c
keywords:
- ContentDistributorDuration Media Player de Windows
topic_type:
- apiref
api_name:
- ContentDistributorDuration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f17bad8ef5dd1ab4b0a3d1c7b5becec6fd34a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700004"
---
# <a name="contentdistributorduration-attribute"></a><span data-ttu-id="ef2c4-104">Atributo ContentDistributorDuration</span><span class="sxs-lookup"><span data-stu-id="ef2c4-104">ContentDistributorDuration Attribute</span></span>

<span data-ttu-id="ef2c4-105">El atributo **ContentDistributorDuration** es la duración de la reproducción del elemento, en segundos.</span><span class="sxs-lookup"><span data-stu-id="ef2c4-105">The **ContentDistributorDuration** attribute is the playing duration of the item, in seconds.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ef2c4-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="ef2c4-106">Applies To</span></span>

-   [<span data-ttu-id="ef2c4-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="ef2c4-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="ef2c4-108">Otros elementos</span><span class="sxs-lookup"><span data-stu-id="ef2c4-108">Other Items</span></span>](other-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="ef2c4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef2c4-109">Remarks</span></span>

<span data-ttu-id="ef2c4-110">Si el atributo **Duration** normal no está establecido (NULL) o 0, se devolverá en su lugar el valor de este atributo.</span><span class="sxs-lookup"><span data-stu-id="ef2c4-110">If the regular **Duration** attribute is either not set (Null) or 0, then the value of this attribute will be returned instead.</span></span>

<span data-ttu-id="ef2c4-111">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ef2c4-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef2c4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef2c4-112">Requirements</span></span>



| <span data-ttu-id="ef2c4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef2c4-113">Requirement</span></span> | <span data-ttu-id="ef2c4-114">Value</span><span class="sxs-lookup"><span data-stu-id="ef2c4-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="ef2c4-115">Versión</span><span class="sxs-lookup"><span data-stu-id="ef2c4-115">Version</span></span><br/> | <span data-ttu-id="ef2c4-116">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="ef2c4-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef2c4-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef2c4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef2c4-118">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="ef2c4-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="ef2c4-119">**Duration (atributo)**</span><span class="sxs-lookup"><span data-stu-id="ef2c4-119">**Duration Attribute**</span></span>](duration-attribute.md)
</dt> </dl>

 

 





