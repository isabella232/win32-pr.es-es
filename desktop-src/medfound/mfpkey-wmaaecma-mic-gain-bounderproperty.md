---
description: Especifica si el DSP de la captura de voz aplica el límite de ganancia de micrófono.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: Propiedad MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705905"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a><span data-ttu-id="5241b-103">\_Propiedad del \_ \_ enlazador de ganancia de WMAAECMA \_ de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="5241b-103">MFPKEY\_WMAAECMA\_MIC\_GAIN\_BOUNDER Property</span></span>

<span data-ttu-id="5241b-104">Especifica si el DSP de la captura de voz aplica el límite de ganancia de micrófono.</span><span class="sxs-lookup"><span data-stu-id="5241b-104">Specifies whether the Voice Capture DSP applies microphone gain bounding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5241b-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5241b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5241b-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="5241b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="5241b-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5241b-107">Data Type</span></span>

<span data-ttu-id="5241b-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="5241b-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="5241b-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="5241b-109">Default Value</span></span>

<span data-ttu-id="5241b-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="5241b-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="5241b-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="5241b-111">Applies To</span></span>

-   [<span data-ttu-id="5241b-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="5241b-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="5241b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5241b-113">Remarks</span></span>

<span data-ttu-id="5241b-114">El límite de ganancia de micrófono garantiza que el micrófono tenga el nivel de ganancia correcto.</span><span class="sxs-lookup"><span data-stu-id="5241b-114">Microphone gain bounding ensures that the microphone has the correct level of gain.</span></span> <span data-ttu-id="5241b-115">Si la ganancia es demasiado alta, la señal capturada podría estar saturada y se recortará.</span><span class="sxs-lookup"><span data-stu-id="5241b-115">If gain is too high, the captured signal might be saturated and will be clipped.</span></span> <span data-ttu-id="5241b-116">El recorte es un efecto no lineal, lo que hará que se produzca un error en el algoritmo de cancelación del eco acústico (AEC).</span><span class="sxs-lookup"><span data-stu-id="5241b-116">Clipping is a non-linear effect, which will cause the acoustic echo cancellation (AEC) algorithm to fail.</span></span> <span data-ttu-id="5241b-117">Si la ganancia es demasiado baja, la relación señal-ruido es baja, lo que también puede provocar un error en el algoritmo AEC o no funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="5241b-117">If the gain is too low, the signal-to-noise ratio is low, which can also cause the AEC algorithm to fail or not perform well.</span></span>

<span data-ttu-id="5241b-118">Esta propiedad puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5241b-118">This property can have the following values.</span></span>



| <span data-ttu-id="5241b-119">Value</span><span class="sxs-lookup"><span data-stu-id="5241b-119">Value</span></span>          | <span data-ttu-id="5241b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="5241b-120">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="5241b-121">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="5241b-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="5241b-122">Habilitar el límite de ganancia de micrófono.</span><span class="sxs-lookup"><span data-stu-id="5241b-122">Enable microphone gain bounding.</span></span>  |
| <span data-ttu-id="5241b-123">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="5241b-123">VARIANT\_FALSE</span></span> | <span data-ttu-id="5241b-124">Deshabilite el límite de ganancia de micrófono.</span><span class="sxs-lookup"><span data-stu-id="5241b-124">Disable microphone gain bounding.</span></span> |



 

<span data-ttu-id="5241b-125">El valor predeterminado de esta propiedad es VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="5241b-125">The default value of this property is VARIANT\_TRUE (enabled).</span></span>

<span data-ttu-id="5241b-126">El límite de ganancia de micrófono solo se aplica cuando el DSP funciona en modo de origen.</span><span class="sxs-lookup"><span data-stu-id="5241b-126">Microphone gain bounding is applies only when the DSP operates in source mode.</span></span> <span data-ttu-id="5241b-127">En el modo de filtro, la aplicación debe asegurarse de que el micrófono tiene el nivel de ganancia correcto.</span><span class="sxs-lookup"><span data-stu-id="5241b-127">In filter mode, the application must ensure that the microphone has the correct gain level.</span></span>

## <a name="requirements"></a><span data-ttu-id="5241b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5241b-128">Requirements</span></span>



| <span data-ttu-id="5241b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5241b-129">Requirement</span></span> | <span data-ttu-id="5241b-130">Value</span><span class="sxs-lookup"><span data-stu-id="5241b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5241b-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5241b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5241b-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5241b-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5241b-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5241b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5241b-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5241b-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5241b-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5241b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5241b-136"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5241b-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5241b-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5241b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5241b-138">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5241b-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5241b-139">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="5241b-139">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
