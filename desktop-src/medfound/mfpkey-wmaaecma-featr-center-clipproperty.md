---
description: Especifica si el DSP de la captura de voz realiza el recorte del centro.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: Propiedad MFPKEY_WMAAECMA_FEATR_CENTER_CLIP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275855"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a><span data-ttu-id="c751e-103">\_Propiedad de \_ \_ \_ recorte del centro de MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="c751e-103">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP Property</span></span>

<span data-ttu-id="c751e-104">Especifica si el DSP de la captura de voz realiza el recorte del centro.</span><span class="sxs-lookup"><span data-stu-id="c751e-104">Specifies whether the Voice Capture DSP performs center clipping.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c751e-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c751e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c751e-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="c751e-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c751e-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c751e-107">Data Type</span></span>

<span data-ttu-id="c751e-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="c751e-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="c751e-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="c751e-109">Default Value</span></span>

<span data-ttu-id="c751e-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="c751e-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="c751e-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="c751e-111">Applies To</span></span>

-   [<span data-ttu-id="c751e-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="c751e-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="c751e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c751e-113">Remarks</span></span>

<span data-ttu-id="c751e-114">El recorte central es un proceso que quita los residuos de eco pequeños que permanecen después del procesamiento de AEC, en situaciones de una sola conversación (cuando la voz solo se produce en un extremo de la línea).</span><span class="sxs-lookup"><span data-stu-id="c751e-114">Center clipping is a process that removes small echo residuals that remain after AEC processing, in single-talk situations (when speech occurs only on one end of the line).</span></span>

<span data-ttu-id="c751e-115">Esta propiedad puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c751e-115">This property can have the following values.</span></span>



| <span data-ttu-id="c751e-116">Value</span><span class="sxs-lookup"><span data-stu-id="c751e-116">Value</span></span>          | <span data-ttu-id="c751e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c751e-117">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="c751e-118">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="c751e-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="c751e-119">Deshabilitar el recorte del centro.</span><span class="sxs-lookup"><span data-stu-id="c751e-119">Disable center clipping.</span></span> |
| <span data-ttu-id="c751e-120">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="c751e-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="c751e-121">Habilitar el recorte del centro.</span><span class="sxs-lookup"><span data-stu-id="c751e-121">Enable center clipping.</span></span>  |



 

<span data-ttu-id="c751e-122">El valor predeterminado de esta propiedad es VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="c751e-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="c751e-123">Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="c751e-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="c751e-124">El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c751e-124">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="c751e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c751e-125">Requirements</span></span>



| <span data-ttu-id="c751e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c751e-126">Requirement</span></span> | <span data-ttu-id="c751e-127">Value</span><span class="sxs-lookup"><span data-stu-id="c751e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c751e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c751e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c751e-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c751e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c751e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c751e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c751e-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c751e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c751e-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c751e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c751e-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c751e-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c751e-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c751e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c751e-135">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c751e-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c751e-136">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="c751e-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
