---
title: Description (atributo, WMP SDK)
description: El atributo Description es una descripción del contenido.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Media Player atributo de descripción de Windows
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699425"
---
# <a name="description-attribute"></a><span data-ttu-id="07a21-104">Descripción (atributo)</span><span class="sxs-lookup"><span data-stu-id="07a21-104">Description Attribute</span></span>

<span data-ttu-id="07a21-105">El atributo **Description** es una descripción del contenido.</span><span class="sxs-lookup"><span data-stu-id="07a21-105">The **Description** attribute is a description of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="07a21-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="07a21-106">Applies To</span></span>

-   [<span data-ttu-id="07a21-107">Archivos de música</span><span class="sxs-lookup"><span data-stu-id="07a21-107">Music Files</span></span>](music-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="07a21-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07a21-108">Remarks</span></span>

<span data-ttu-id="07a21-109">Este atributo se almacena en archivos de música, no en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="07a21-109">This attribute is stored in music files, not in the library.</span></span>

<span data-ttu-id="07a21-110">Este atributo puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="07a21-110">This attribute may have multiple values.</span></span> <span data-ttu-id="07a21-111">Para recuperar todos los valores de un atributo con varios valores, debe utilizar los *medios*. método **getItemInfoByType** , no el método *media*. getItemInfo.</span><span class="sxs-lookup"><span data-stu-id="07a21-111">To retrieve all of the values for a multi-valued attribute, you must use the *Media*.**getItemInfoByType** method, not the *Media*.getItemInfo method.</span></span>

<span data-ttu-id="07a21-112">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMDescription.</span><span class="sxs-lookup"><span data-stu-id="07a21-112">The Windows Media Format SDK constant for this attribute is g\_wszWMDescription.</span></span>

<span data-ttu-id="07a21-113">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="07a21-113">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07a21-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07a21-114">Requirements</span></span>



| <span data-ttu-id="07a21-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="07a21-115">Requirement</span></span> | <span data-ttu-id="07a21-116">Value</span><span class="sxs-lookup"><span data-stu-id="07a21-116">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="07a21-117">Versión</span><span class="sxs-lookup"><span data-stu-id="07a21-117">Version</span></span><br/> | <span data-ttu-id="07a21-118">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="07a21-118">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07a21-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="07a21-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a21-120">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="07a21-120">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





