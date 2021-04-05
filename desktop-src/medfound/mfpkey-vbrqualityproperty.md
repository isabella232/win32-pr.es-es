---
description: Especifica el nivel de calidad real de la codificación de velocidad de bits variable (VBR) basada en la calidad (1-paso).
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: Propiedad MFPKEY_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dff57fc27b952780737d63fa8f04faf722ed8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001624"
---
# <a name="mfpkey_vbrquality-property"></a><span data-ttu-id="c64c0-103">\_Propiedad VBRQUALITY de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="c64c0-103">MFPKEY\_VBRQUALITY Property</span></span>

<span data-ttu-id="c64c0-104">Especifica el nivel de calidad real de la codificación de velocidad de bits variable (VBR) basada en la calidad (1-paso).</span><span class="sxs-lookup"><span data-stu-id="c64c0-104">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c64c0-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c64c0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c64c0-106">g \_ wszWMVCVBRQuality, g \_ wszWMCPAudioVBRQuality</span><span class="sxs-lookup"><span data-stu-id="c64c0-106">g\_wszWMVCVBRQuality, g\_wszWMCPAudioVBRQuality</span></span>

## <a name="data-type"></a><span data-ttu-id="c64c0-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c64c0-107">Data Type</span></span>

<span data-ttu-id="c64c0-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c64c0-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="c64c0-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c64c0-109">Remarks</span></span>

<span data-ttu-id="c64c0-110">No todos los valores del intervalo tienen un significado único.</span><span class="sxs-lookup"><span data-stu-id="c64c0-110">Not all of the values in the range have a unique meaning.</span></span> <span data-ttu-id="c64c0-111">Los valores que representan un paso en la calidad del nivel anterior son: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97 y 100.</span><span class="sxs-lookup"><span data-stu-id="c64c0-111">The values that represent a step up in quality from the previous level are: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, and 100.</span></span>

<span data-ttu-id="c64c0-112">En el caso de los objetos de codificador de audio, los modos de calidad se proporcionan en la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) de los tipos de salida que se recuperan mediante [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span><span class="sxs-lookup"><span data-stu-id="c64c0-112">For audio encoder objects, the quality modes are provided in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the output types that you retrieve using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).</span></span>

## <a name="requirements"></a><span data-ttu-id="c64c0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c64c0-113">Requirements</span></span>



| <span data-ttu-id="c64c0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c64c0-114">Requirement</span></span> | <span data-ttu-id="c64c0-115">Value</span><span class="sxs-lookup"><span data-stu-id="c64c0-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c64c0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c64c0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c64c0-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c64c0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c64c0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c64c0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c64c0-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c64c0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c64c0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c64c0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c64c0-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c64c0-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c64c0-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c64c0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c64c0-123">Enumeración de los tipos de audio para los modos de codificación específicos</span><span class="sxs-lookup"><span data-stu-id="c64c0-123">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[<span data-ttu-id="c64c0-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c64c0-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
