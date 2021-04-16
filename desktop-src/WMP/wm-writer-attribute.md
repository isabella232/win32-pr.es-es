---
title: Atributo WM/escritor
description: El atributo WM/Writer es el nombre del escritor que escribió las palabras del contenido.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- Windows atributo de WM/escritor Media Player
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29aabf353fc742370ac5d01f084544be8143d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649927"
---
# <a name="wmwriter-attribute"></a><span data-ttu-id="b8d21-104">Atributo WM/escritor</span><span class="sxs-lookup"><span data-stu-id="b8d21-104">WM/Writer Attribute</span></span>

<span data-ttu-id="b8d21-105">El atributo **WM/Writer** es el nombre del escritor que escribió las palabras del contenido.</span><span class="sxs-lookup"><span data-stu-id="b8d21-105">The **WM/Writer** attribute is the name of the writer who wrote the words of the content.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b8d21-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="b8d21-106">Applies To</span></span>

-   [<span data-ttu-id="b8d21-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="b8d21-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="b8d21-108">Atributos de archivo de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="b8d21-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="b8d21-109">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="b8d21-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="b8d21-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8d21-110">Remarks</span></span>

<span data-ttu-id="b8d21-111">Este atributo se almacena en la biblioteca y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="b8d21-111">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="b8d21-112">Este atributo puede tener varios valores.</span><span class="sxs-lookup"><span data-stu-id="b8d21-112">This attribute may have multiple values.</span></span> <span data-ttu-id="b8d21-113">Para recuperar todos los valores de un atributo con varios valores, debe usar el método **media. getItemInfoByType** , no el método **media. getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="b8d21-113">To retrieve all of the values for a multi-valued attribute, you must use the **Media.getItemInfoByType** method, not the **Media.getItemInfo** method.</span></span>

<span data-ttu-id="b8d21-114">**Writer** es un alias para este atributo.</span><span class="sxs-lookup"><span data-stu-id="b8d21-114">**Writer** is an alias for this attribute.</span></span>

<span data-ttu-id="b8d21-115">La constante del SDK de Windows Media Format para este atributo es g \_ wszWMWriter.</span><span class="sxs-lookup"><span data-stu-id="b8d21-115">The Windows Media Format SDK constant for this attribute is g\_wszWMWriter.</span></span>

<span data-ttu-id="b8d21-116">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="b8d21-116">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d21-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8d21-117">Requirements</span></span>



| <span data-ttu-id="b8d21-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8d21-118">Requirement</span></span> | <span data-ttu-id="b8d21-119">Value</span><span class="sxs-lookup"><span data-stu-id="b8d21-119">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b8d21-120">Versión</span><span class="sxs-lookup"><span data-stu-id="b8d21-120">Version</span></span><br/> | <span data-ttu-id="b8d21-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="b8d21-121">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8d21-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8d21-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d21-123">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="b8d21-123">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="b8d21-124">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="b8d21-124">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> </dl>

 

 





