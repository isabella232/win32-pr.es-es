---
description: Especifica si el DSP de la captura de voz realiza el relleno de ruido.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: Propiedad MFPKEY_WMAAECMA_FEATR_NOISE_FILL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705908"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a><span data-ttu-id="104bf-103">\_Propiedad de \_ relleno de \_ ruido \_ de MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="104bf-103">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL Property</span></span>

<span data-ttu-id="104bf-104">Especifica si el DSP de la captura de voz realiza el relleno de ruido.</span><span class="sxs-lookup"><span data-stu-id="104bf-104">Specifies whether the Voice Capture DSP performs noise filling.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="104bf-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="104bf-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="104bf-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="104bf-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="104bf-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="104bf-107">Data Type</span></span>

<span data-ttu-id="104bf-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="104bf-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="104bf-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="104bf-109">Default Value</span></span>

<span data-ttu-id="104bf-110">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="104bf-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="104bf-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="104bf-111">Applies To</span></span>

-   [<span data-ttu-id="104bf-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="104bf-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="104bf-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="104bf-113">Remarks</span></span>

<span data-ttu-id="104bf-114">El relleno de ruido agrega una pequeña cantidad de ruido a partes de la señal en las que el recorte del centro ha quitado los ecos residuales.</span><span class="sxs-lookup"><span data-stu-id="104bf-114">Noise filling adds a small amount of noise to portions of the signal where center clipping has removed the residual echoes.</span></span> <span data-ttu-id="104bf-115">Esto da como resultado una mejor experiencia para el usuario que la salida de brechas silenciosas en la señal.</span><span class="sxs-lookup"><span data-stu-id="104bf-115">This results in a better experience for the user than leaving silent gaps in the signal.</span></span>

<span data-ttu-id="104bf-116">Esta propiedad puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="104bf-116">This property can have the following values.</span></span>



| <span data-ttu-id="104bf-117">Value</span><span class="sxs-lookup"><span data-stu-id="104bf-117">Value</span></span>          | <span data-ttu-id="104bf-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="104bf-118">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="104bf-119">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="104bf-119">VARIANT\_TRUE</span></span>  | <span data-ttu-id="104bf-120">Habilitar el relleno de ruido.</span><span class="sxs-lookup"><span data-stu-id="104bf-120">Enable noise filling.</span></span>  |
| <span data-ttu-id="104bf-121">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="104bf-121">VARIANT\_FALSE</span></span> | <span data-ttu-id="104bf-122">Deshabilitar el relleno de ruido.</span><span class="sxs-lookup"><span data-stu-id="104bf-122">Disable noise filling.</span></span> |



 

<span data-ttu-id="104bf-123">El valor predeterminado de esta propiedad es VARIANT \_ true (Enabled).</span><span class="sxs-lookup"><span data-stu-id="104bf-123">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="104bf-124">Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="104bf-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="104bf-125">El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="104bf-125">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="104bf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="104bf-126">Requirements</span></span>



| <span data-ttu-id="104bf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="104bf-127">Requirement</span></span> | <span data-ttu-id="104bf-128">Value</span><span class="sxs-lookup"><span data-stu-id="104bf-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="104bf-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="104bf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="104bf-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="104bf-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="104bf-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="104bf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="104bf-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="104bf-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="104bf-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="104bf-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="104bf-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="104bf-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="104bf-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="104bf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="104bf-136">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="104bf-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="104bf-137">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="104bf-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
