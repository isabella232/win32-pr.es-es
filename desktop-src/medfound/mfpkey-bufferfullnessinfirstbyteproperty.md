---
description: Especifica si la secuencia de bits de vídeo codificada contiene un valor de llenado de búfer con cada fotograma clave.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: Propiedad MFPKEY_BUFFERFULLNESSINFIRSTBYTE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697698"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a><span data-ttu-id="62f8c-103">\_Propiedad BUFFERFULLNESSINFIRSTBYTE de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="62f8c-103">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE Property</span></span>

<span data-ttu-id="62f8c-104">Especifica si la secuencia de bits de vídeo codificada contiene un valor de llenado de búfer con cada fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="62f8c-104">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="62f8c-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="62f8c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="62f8c-106">g \_ wszWMVCBufferFullnessInFirstByte</span><span class="sxs-lookup"><span data-stu-id="62f8c-106">g\_wszWMVCBufferFullnessInFirstByte</span></span>

## <a name="data-type"></a><span data-ttu-id="62f8c-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="62f8c-107">Data Type</span></span>

<span data-ttu-id="62f8c-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="62f8c-108">VT\_BOOL</span></span>

## <a name="remarks"></a><span data-ttu-id="62f8c-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62f8c-109">Remarks</span></span>

<span data-ttu-id="62f8c-110">Debe establecer un tipo de salida antes de obtener este valor.</span><span class="sxs-lookup"><span data-stu-id="62f8c-110">You must set an output type before getting this value.</span></span>

<span data-ttu-id="62f8c-111">Puede obtener el valor de esta propiedad mediante [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span><span class="sxs-lookup"><span data-stu-id="62f8c-111">You can get the value of this property using [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="62f8c-112">Si usa **IPropertyBag**, primero debe establecer el valor de FourCC del formato comprimido deseado con la propiedad [ \_ FourCC MFPKEY](mfpkey-fourccproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="62f8c-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format with the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

<span data-ttu-id="62f8c-113">Tener el llenado del búfer en el primer byte de todos los fotogramas clave permite determinar el tamaño de búfer necesario al concatenar secuencias de vídeo comprimidas.</span><span class="sxs-lookup"><span data-stu-id="62f8c-113">Having the buffer fullness in the first byte of all key frames enables you to determine the buffer size required when concatenating compressed video streams.</span></span>

## <a name="requirements"></a><span data-ttu-id="62f8c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62f8c-114">Requirements</span></span>



| <span data-ttu-id="62f8c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="62f8c-115">Requirement</span></span> | <span data-ttu-id="62f8c-116">Value</span><span class="sxs-lookup"><span data-stu-id="62f8c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62f8c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62f8c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="62f8c-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="62f8c-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="62f8c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62f8c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="62f8c-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="62f8c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62f8c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62f8c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="62f8c-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="62f8c-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62f8c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="62f8c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f8c-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62f8c-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




