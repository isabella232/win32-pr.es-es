---
title: Atributo AverageLevel
description: El atributo AverageLevel es un valor de amplitud de 16 bits que indica el nivel de volumen medio.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- AverageLevel Media Player de Windows
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594612f3675d818f94270b1952d2a9ca7bed15d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699426"
---
# <a name="averagelevel-attribute"></a><span data-ttu-id="07cd7-104">Atributo AverageLevel</span><span class="sxs-lookup"><span data-stu-id="07cd7-104">AverageLevel Attribute</span></span>

<span data-ttu-id="07cd7-105">El atributo **AverageLevel** es un valor de amplitud de 16 bits que indica el nivel de volumen medio.</span><span class="sxs-lookup"><span data-stu-id="07cd7-105">The **AverageLevel** attribute is a 16-bit amplitude value indicating the average volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="07cd7-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="07cd7-106">Applies To</span></span>

-   [<span data-ttu-id="07cd7-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="07cd7-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="07cd7-108">Archivos de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="07cd7-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="07cd7-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07cd7-109">Remarks</span></span>

<span data-ttu-id="07cd7-110">Este atributo se almacena en la biblioteca y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="07cd7-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="07cd7-111">Windows Media Player establece este valor en cualquiera de las instancias siguientes:</span><span class="sxs-lookup"><span data-stu-id="07cd7-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="07cd7-112">Una vez que haya copiado un archivo.</span><span class="sxs-lookup"><span data-stu-id="07cd7-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="07cd7-113">Una vez que haya reproducido un archivo (cuando la mejora de la nivelación de volumen automática está habilitada).</span><span class="sxs-lookup"><span data-stu-id="07cd7-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="07cd7-114">La constante del SDK de Windows Media Format para este atributo es g \_ wszAverageLevel.</span><span class="sxs-lookup"><span data-stu-id="07cd7-114">The Windows Media Format SDK constant for this attribute is g\_wszAverageLevel.</span></span>

<span data-ttu-id="07cd7-115">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="07cd7-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07cd7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07cd7-116">Requirements</span></span>



| <span data-ttu-id="07cd7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="07cd7-117">Requirement</span></span> | <span data-ttu-id="07cd7-118">Value</span><span class="sxs-lookup"><span data-stu-id="07cd7-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="07cd7-119">Versión</span><span class="sxs-lookup"><span data-stu-id="07cd7-119">Version</span></span><br/> | <span data-ttu-id="07cd7-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="07cd7-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07cd7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="07cd7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07cd7-122">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="07cd7-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





