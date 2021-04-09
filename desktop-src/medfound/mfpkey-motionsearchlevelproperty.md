---
description: Especifica cómo se utiliza la información de color en las operaciones de búsqueda de movimiento.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: Propiedad MFPKEY_MOTIONSEARCHLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082472"
---
# <a name="mfpkey_motionsearchlevel-property"></a><span data-ttu-id="60199-103">\_Propiedad MOTIONSEARCHLEVEL de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="60199-103">MFPKEY\_MOTIONSEARCHLEVEL Property</span></span>

<span data-ttu-id="60199-104">Especifica cómo se utiliza la información de color en las operaciones de búsqueda de movimiento.</span><span class="sxs-lookup"><span data-stu-id="60199-104">Specifies how color information is used in motion search operations.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="60199-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="60199-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="60199-106">g \_ wszWMVCMotionSearchLevel</span><span class="sxs-lookup"><span data-stu-id="60199-106">g\_wszWMVCMotionSearchLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="60199-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="60199-107">Data Type</span></span>

<span data-ttu-id="60199-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="60199-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="60199-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="60199-109">Default Value</span></span>

<span data-ttu-id="60199-110">0</span><span class="sxs-lookup"><span data-stu-id="60199-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="60199-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60199-111">Remarks</span></span>

<span data-ttu-id="60199-112">Esta propiedad se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="60199-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="60199-113">Value</span><span class="sxs-lookup"><span data-stu-id="60199-113">Value</span></span> | <span data-ttu-id="60199-114">Información de vídeo usada</span><span class="sxs-lookup"><span data-stu-id="60199-114">Video information used</span></span>                           |
|-------|--------------------------------------------------|
| <span data-ttu-id="60199-115">0</span><span class="sxs-lookup"><span data-stu-id="60199-115">0</span></span>     | <span data-ttu-id="60199-116">Solo luminancia.</span><span class="sxs-lookup"><span data-stu-id="60199-116">Luma only.</span></span>                                       |
| <span data-ttu-id="60199-117">1</span><span class="sxs-lookup"><span data-stu-id="60199-117">1</span></span>     | <span data-ttu-id="60199-118">Luminancia con intensidad de croma entero más próximo.</span><span class="sxs-lookup"><span data-stu-id="60199-118">Luma with nearest-integer chroma.</span></span>                |
| <span data-ttu-id="60199-119">2</span><span class="sxs-lookup"><span data-stu-id="60199-119">2</span></span>     | <span data-ttu-id="60199-120">Luminancia con intensidad de color verdadero.</span><span class="sxs-lookup"><span data-stu-id="60199-120">Luma with true chroma.</span></span>                           |
| <span data-ttu-id="60199-121">-1</span><span class="sxs-lookup"><span data-stu-id="60199-121">-1</span></span>    | <span data-ttu-id="60199-122">Adaptativo macrobloque: adaptable con intensidad de croma real.</span><span class="sxs-lookup"><span data-stu-id="60199-122">Macroblock-adaptive with true chroma.</span></span>            |
| <span data-ttu-id="60199-123">-2</span><span class="sxs-lookup"><span data-stu-id="60199-123">-2</span></span>    | <span data-ttu-id="60199-124">Adaptativo macrobloque: adaptable con el cromado de entero más próximo.</span><span class="sxs-lookup"><span data-stu-id="60199-124">Macroblock-adaptive with nearest-integer chroma.</span></span> |



 

<span data-ttu-id="60199-125">De forma predeterminada, el códec realiza la búsqueda de movimiento solo en el canal de luminancia.</span><span class="sxs-lookup"><span data-stu-id="60199-125">By default, the codec performs motion search only in the luma channel.</span></span> <span data-ttu-id="60199-126">La inclusión de información de croma en la estimación de movimiento puede mejorar significativamente la calidad del vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="60199-126">Including chroma information in motion estimation can significantly improve the quality of encoded video.</span></span> <span data-ttu-id="60199-127">La búsqueda de movimiento con luminancia y intensidad de croma real producirá la mejor calidad de vídeo, pero con el mayor costo de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="60199-127">Motion search with luma and true chroma will yield the best video quality, but at the highest performance cost.</span></span> <span data-ttu-id="60199-128">Los dos modos dinámicos (-1 y-2) y la luminancia con el modo de croma de entero más próximo proporcionarán un riesgo razonable entre calidad y rendimiento.</span><span class="sxs-lookup"><span data-stu-id="60199-128">The two dynamic modes (-1 and -2) and the luma with nearest-integer chroma mode will provide reasonable compromises between quality and performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="60199-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60199-129">Requirements</span></span>



| <span data-ttu-id="60199-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="60199-130">Requirement</span></span> | <span data-ttu-id="60199-131">Value</span><span class="sxs-lookup"><span data-stu-id="60199-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60199-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60199-132">Minimum supported client</span></span><br/> | <span data-ttu-id="60199-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="60199-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="60199-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60199-134">Minimum supported server</span></span><br/> | <span data-ttu-id="60199-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="60199-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="60199-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60199-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="60199-137"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="60199-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60199-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="60199-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60199-139">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="60199-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




