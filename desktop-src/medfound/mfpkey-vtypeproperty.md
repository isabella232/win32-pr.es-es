---
description: Especifica la lógica que el códec usará para detectar vídeo de origen entrelazado.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: Propiedad MFPKEY_VTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908386"
---
# <a name="mfpkey_vtype-property"></a><span data-ttu-id="d687f-103">\_Propiedad VTYPE de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="d687f-103">MFPKEY\_VTYPE Property</span></span>

<span data-ttu-id="d687f-104">Especifica la lógica que el códec usará para detectar vídeo de origen entrelazado.</span><span class="sxs-lookup"><span data-stu-id="d687f-104">Specifies the logic that the codec will use to detect interlaced source video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d687f-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d687f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d687f-106">g \_ wszWMVCVType</span><span class="sxs-lookup"><span data-stu-id="d687f-106">g\_wszWMVCVType</span></span>

## <a name="data-type"></a><span data-ttu-id="d687f-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d687f-107">Data Type</span></span>

<span data-ttu-id="d687f-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d687f-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="d687f-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="d687f-109">Default Value</span></span>

<span data-ttu-id="d687f-110">0</span><span class="sxs-lookup"><span data-stu-id="d687f-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="d687f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d687f-111">Remarks</span></span>

<span data-ttu-id="d687f-112">Esta propiedad se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d687f-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="d687f-113">Value</span><span class="sxs-lookup"><span data-stu-id="d687f-113">Value</span></span> | <span data-ttu-id="d687f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d687f-114">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d687f-115">0</span><span class="sxs-lookup"><span data-stu-id="d687f-115">0</span></span>     | <span data-ttu-id="d687f-116">El códec usará la lógica de detección estándar de tipo de marco.</span><span class="sxs-lookup"><span data-stu-id="d687f-116">The codec will use the standard frame-type detection logic.</span></span>                                                                                 |
| <span data-ttu-id="d687f-117">1</span><span class="sxs-lookup"><span data-stu-id="d687f-117">1</span></span>     | <span data-ttu-id="d687f-118">El códec tratará todos los fotogramas de vídeo de origen como fotogramas entrelazados.</span><span class="sxs-lookup"><span data-stu-id="d687f-118">The codec will treat all source video frames as interlaced frames.</span></span>                                                                          |
| <span data-ttu-id="d687f-119">2</span><span class="sxs-lookup"><span data-stu-id="d687f-119">2</span></span>     | <span data-ttu-id="d687f-120">El códec tratará todos los fotogramas de vídeo de origen como campos de vídeo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="d687f-120">The codec will treat all source video frames as fields of interlaced video.</span></span>                                                                 |
| <span data-ttu-id="d687f-121">3</span><span class="sxs-lookup"><span data-stu-id="d687f-121">3</span></span>     | <span data-ttu-id="d687f-122">El códec determinará automáticamente si los fotogramas de vídeo de entrada son fotogramas entrelazados o campos de vídeo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="d687f-122">The codec will automatically determine whether input video frames are interlaced frames or fields of interlaced video.</span></span>                      |
| <span data-ttu-id="d687f-123">4</span><span class="sxs-lookup"><span data-stu-id="d687f-123">4</span></span>     | <span data-ttu-id="d687f-124">El códec determinará automáticamente si los fotogramas de vídeo de entrada son fotogramas progresivos, fotogramas entrelazados o campos de vídeo entrelazado.</span><span class="sxs-lookup"><span data-stu-id="d687f-124">The codec will automatically determine whether input video frames are progressive frames, interlaced frames, or fields of interlaced video.</span></span> |



 

<span data-ttu-id="d687f-125">Esta propiedad determina el método de codificación de imágenes que se usa para la codificación de vídeo progresiva o entrelazada.</span><span class="sxs-lookup"><span data-stu-id="d687f-125">This property determines the picture encoding method used for progressive or interlaced video encoding.</span></span>

<span data-ttu-id="d687f-126">Si no se especifica ningún tipo de vídeo, el códec utilizará la codificación de tramas progresiva para las sesiones de codificación progresiva y la codificación entrelazada de campo para las sesiones de codificación entrelazada.</span><span class="sxs-lookup"><span data-stu-id="d687f-126">If no video type is specified, the codec will use progressive frame encoding for progressive encoding sessions, and field interlaced encoding for interlaced encoding sessions.</span></span> <span data-ttu-id="d687f-127">El tipo de sesión de codificación de vídeo (progresivo o entrelazado) se establece mediante la [propiedad \_ INTERLACEDCODINGENABLED de MFPKEY](mfpkey-interlacedcodingenabledproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="d687f-127">The type of video encoding session (progressive or interlaced) is set by using the [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="d687f-128">La propiedad [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) debe establecerse en Variant \_ true para producir una salida entrelazada; de lo contrario, el establecimiento de la \_ propiedad MPFKEY VTYPE no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="d687f-128">The [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property must be set to VARIANT\_TRUE in order to produce interlaced output; otherwise, setting the MPFKEY\_VTYPE property will have no effect.</span></span>

 

<span data-ttu-id="d687f-129">Cuando se está codificando el vídeo entrelazado, es posible especificar varios métodos de codificación de imágenes.</span><span class="sxs-lookup"><span data-stu-id="d687f-129">When interlaced video is being encoded, it is possible to specify several picture encoding methods.</span></span> <span data-ttu-id="d687f-130">Normalmente, la manera más eficaz de codificar vídeo entrelazado es usar el método entrelazado de campo (2).</span><span class="sxs-lookup"><span data-stu-id="d687f-130">Typically the most efficient way to encode interlaced video is to use the field interlaced method (2).</span></span> <span data-ttu-id="d687f-131">Si el vídeo de origen contiene muy poco movimiento, el método entrelazado de fotogramas (1) o el método de marco/campo automático (2) podrían ser más adecuados.</span><span class="sxs-lookup"><span data-stu-id="d687f-131">If the source video contains very little motion, the frame interlaced method (1) or the auto frame/field method (2) might be more suitable.</span></span>

<span data-ttu-id="d687f-132">Al codificar contenido mixto (que contiene fotogramas progresivos y entrelazados), es mejor usar el método automático de valor Frame/Field/progresivo (4).</span><span class="sxs-lookup"><span data-stu-id="d687f-132">When encoding mixed content (containing both progressive and interlaced frames), it's best to use the value auto frame/field/progressive method (4).</span></span>

## <a name="requirements"></a><span data-ttu-id="d687f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d687f-133">Requirements</span></span>



| <span data-ttu-id="d687f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d687f-134">Requirement</span></span> | <span data-ttu-id="d687f-135">Value</span><span class="sxs-lookup"><span data-stu-id="d687f-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d687f-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d687f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d687f-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d687f-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d687f-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d687f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d687f-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d687f-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d687f-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d687f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d687f-141"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d687f-141"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d687f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="d687f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d687f-143">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d687f-143">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




