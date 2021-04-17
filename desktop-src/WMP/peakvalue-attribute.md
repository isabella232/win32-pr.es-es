---
title: Atributo PeakValue
description: El atributo PeakValue es un valor de amplitud de 16 bits que indica el nivel de volumen máximo.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- PeakValue Media Player de Windows
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700256"
---
# <a name="peakvalue-attribute"></a><span data-ttu-id="16a4c-104">Atributo PeakValue</span><span class="sxs-lookup"><span data-stu-id="16a4c-104">PeakValue Attribute</span></span>

<span data-ttu-id="16a4c-105">El atributo **PeakValue** es un valor de amplitud de 16 bits que indica el nivel de volumen máximo.</span><span class="sxs-lookup"><span data-stu-id="16a4c-105">The **PeakValue** attribute is a 16-bit amplitude value indicating the peak volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="16a4c-106">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="16a4c-106">Applies To</span></span>

-   [<span data-ttu-id="16a4c-107">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="16a4c-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="16a4c-108">Archivos de Windows Media de uso frecuente</span><span class="sxs-lookup"><span data-stu-id="16a4c-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="16a4c-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16a4c-109">Remarks</span></span>

<span data-ttu-id="16a4c-110">Este atributo se almacena en la biblioteca y en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="16a4c-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="16a4c-111">Windows Media Player establece este valor en cualquiera de las instancias siguientes:</span><span class="sxs-lookup"><span data-stu-id="16a4c-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="16a4c-112">Una vez que haya copiado un archivo.</span><span class="sxs-lookup"><span data-stu-id="16a4c-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="16a4c-113">Una vez que haya reproducido un archivo (cuando la mejora de la nivelación de volumen automática está habilitada).</span><span class="sxs-lookup"><span data-stu-id="16a4c-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="16a4c-114">La constante del SDK de Windows Media Format para este atributo es g \_ wszPeakValue.</span><span class="sxs-lookup"><span data-stu-id="16a4c-114">The Windows Media Format SDK constant for this attribute is g\_wszPeakValue.</span></span>

<span data-ttu-id="16a4c-115">Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="16a4c-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="16a4c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16a4c-116">Requirements</span></span>



| <span data-ttu-id="16a4c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="16a4c-117">Requirement</span></span> | <span data-ttu-id="16a4c-118">Value</span><span class="sxs-lookup"><span data-stu-id="16a4c-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="16a4c-119">Versión</span><span class="sxs-lookup"><span data-stu-id="16a4c-119">Version</span></span><br/> | <span data-ttu-id="16a4c-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="16a4c-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16a4c-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="16a4c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a4c-122">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="16a4c-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





