---
title: Atributo WM/Language
description: El atributo WM/Language es el idioma del elemento.
ms.assetid: aebfb518-61ca-4b75-875a-ce2127a74b67
keywords:
- Windows atributo WM/idioma Media Player
topic_type:
- apiref
api_name:
- WM/Language
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172cc8498bf5360e29822a484bcc2ddacd70b8b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708716"
---
# <a name="wmlanguage-attribute"></a><span data-ttu-id="314f7-104">Atributo WM/Language</span><span class="sxs-lookup"><span data-stu-id="314f7-104">WM/Language Attribute</span></span>

<span data-ttu-id="314f7-105">El atributo **WM/Language** es el idioma del elemento.</span><span class="sxs-lookup"><span data-stu-id="314f7-105">The **WM/Language** attribute is the language of the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="314f7-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="314f7-106">Applies To</span></span>

-   [<span data-ttu-id="314f7-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="314f7-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="314f7-108">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="314f7-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="314f7-109">Elementos de radio</span><span class="sxs-lookup"><span data-stu-id="314f7-109">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="314f7-110">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="314f7-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="314f7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="314f7-111">Remarks</span></span>

<span data-ttu-id="314f7-112">Este atributo se almacena en la biblioteca y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="314f7-112">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="314f7-113">Este atributo puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="314f7-113">This attribute may have multiple values.</span></span> <span data-ttu-id="314f7-114">Para recuperar todos los valores de un atributo con varios valores, debe usar el método **media. getItemInfoByType** , no el método **media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="314f7-114">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="314f7-115">**Language** es un alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="314f7-115">**Language** is an alias for this attribute.</span></span>

<span data-ttu-id="314f7-116">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMLanguage.</span><span class="sxs-lookup"><span data-stu-id="314f7-116">The Windows Media Format SDK constant for this attribute is g\_wszWMLanguage.</span></span>

<span data-ttu-id="314f7-117">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="314f7-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="314f7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="314f7-118">Requirements</span></span>



| <span data-ttu-id="314f7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="314f7-119">Requirement</span></span> | <span data-ttu-id="314f7-120">Value</span><span class="sxs-lookup"><span data-stu-id="314f7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="314f7-121">Versión</span><span class="sxs-lookup"><span data-stu-id="314f7-121">Version</span></span><br/> | <span data-ttu-id="314f7-122">Windows Media Player 9 series o posterior (el elemento de radio solo se admite en Windows Media Player 9 series)</span><span class="sxs-lookup"><span data-stu-id="314f7-122">Windows Media Player 9 Series or later (The radio item is supported only in Windows Media Player 9 Series)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="314f7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="314f7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314f7-124">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="314f7-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="314f7-125">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="314f7-125">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





