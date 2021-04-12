---
description: Especifica cómo el DSP de la captura de voz realiza el procesamiento de la matriz de micrófono.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: Propiedad MFPKEY_WMAAECMA_FEATR_MICARR_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf8ffcae465e8abfddedb3e6d6dded683bb2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275853"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a><span data-ttu-id="5ddee-103">MFPKEY \_ WMAAECMA \_ feat \_ MICARR \_ Mode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5ddee-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE Property</span></span>

<span data-ttu-id="5ddee-104">Especifica cómo el DSP de la captura de voz realiza el procesamiento de la matriz de micrófono.</span><span class="sxs-lookup"><span data-stu-id="5ddee-104">Specifies how the Voice Capture DSP performs microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5ddee-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5ddee-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5ddee-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="5ddee-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="5ddee-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5ddee-107">Data Type</span></span>

<span data-ttu-id="5ddee-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="5ddee-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="5ddee-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="5ddee-109">Default Value</span></span>

<span data-ttu-id="5ddee-110">MICARRAY de \_ un solo \_ rayo</span><span class="sxs-lookup"><span data-stu-id="5ddee-110">MICARRAY\_SINGLE\_BEAM</span></span>

## <a name="applies-to"></a><span data-ttu-id="5ddee-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="5ddee-111">Applies To</span></span>

-   [<span data-ttu-id="5ddee-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="5ddee-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="5ddee-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ddee-113">Remarks</span></span>

<span data-ttu-id="5ddee-114">El valor de esta propiedad es un miembro de la enumeración de [ \_ \_ modo de matriz de MIC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) .</span><span class="sxs-lookup"><span data-stu-id="5ddee-114">The value of this property is a member of the [MIC\_ARRAY\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) enumeration.</span></span> <span data-ttu-id="5ddee-115">El valor predeterminado es MICARRAY de \_ un solo \_ rayo.</span><span class="sxs-lookup"><span data-stu-id="5ddee-115">The default value is MICARRAY\_SINGLE\_BEAM.</span></span> <span data-ttu-id="5ddee-116">Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="5ddee-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="5ddee-117">El DSP usa esta propiedad solo cuando está habilitado el procesamiento de la matriz de micrófono.</span><span class="sxs-lookup"><span data-stu-id="5ddee-117">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ddee-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ddee-118">Requirements</span></span>



| <span data-ttu-id="5ddee-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ddee-119">Requirement</span></span> | <span data-ttu-id="5ddee-120">Value</span><span class="sxs-lookup"><span data-stu-id="5ddee-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ddee-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ddee-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5ddee-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5ddee-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5ddee-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ddee-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5ddee-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ddee-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5ddee-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ddee-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ddee-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ddee-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ddee-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ddee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ddee-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5ddee-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5ddee-129">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="5ddee-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
