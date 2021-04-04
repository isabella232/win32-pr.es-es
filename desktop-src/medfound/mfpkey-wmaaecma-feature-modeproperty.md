---
description: Permite que la aplicación invalide la configuración predeterminada en varias propiedades del DSP de captura de voz.
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: Propiedad MFPKEY_WMAAECMA_FEATURE_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811618"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a><span data-ttu-id="cea68-103">\_Propiedad del \_ modo de característica MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="cea68-103">MFPKEY\_WMAAECMA\_FEATURE\_MODE Property</span></span>

<span data-ttu-id="cea68-104">Permite que la aplicación invalide la configuración predeterminada en varias propiedades del DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="cea68-104">Enables the application to override the default settings on various properties of the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cea68-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="cea68-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cea68-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="cea68-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="cea68-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="cea68-107">Data Type</span></span>

<span data-ttu-id="cea68-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="cea68-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="cea68-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="cea68-109">Default Value</span></span>

<span data-ttu-id="cea68-110">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="cea68-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="cea68-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="cea68-111">Applies To</span></span>

-   [<span data-ttu-id="cea68-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="cea68-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="cea68-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cea68-113">Remarks</span></span>

<span data-ttu-id="cea68-114">Si esta propiedad es VARIANT \_ true, la aplicación puede establecer las siguientes propiedades en el DSP:</span><span class="sxs-lookup"><span data-stu-id="cea68-114">If this property is VARIANT\_TRUE, the application can set the following properties on the DSP:</span></span>

-   [<span data-ttu-id="cea68-115">MFPKEY \_ WMAAECMA \_ feat \_ AES</span><span class="sxs-lookup"><span data-stu-id="cea68-115">MFPKEY\_WMAAECMA\_FEATR\_AES</span></span>](mfpkey-wmaaecma-featr-aesproperty.md)
-   [<span data-ttu-id="cea68-116">MFPKEY \_ WMAAECMA \_ feat \_ AGC</span><span class="sxs-lookup"><span data-stu-id="cea68-116">MFPKEY\_WMAAECMA\_FEATR\_AGC</span></span>](mfpkey-wmaaecma-featr-agcproperty.md)
-   [<span data-ttu-id="cea68-117">\_clip del \_ \_ Centro \_ de MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="cea68-117">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP</span></span>](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [<span data-ttu-id="cea68-118">\_longitud del \_ eco del funcdor de MFPKEY WMAAECMA \_ \_</span><span class="sxs-lookup"><span data-stu-id="cea68-118">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH</span></span>](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [<span data-ttu-id="cea68-119">\_tamaño de \_ \_ marco \_ del MFPKEY de WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="cea68-119">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE</span></span>](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [<span data-ttu-id="cea68-120">\_ \_ \_ modo MICARR MFPKEY WMAAECMA feat \_</span><span class="sxs-lookup"><span data-stu-id="cea68-120">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE</span></span>](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [<span data-ttu-id="cea68-121">MFPKEY \_ WMAAECMA \_ feat \_ MICARR \_ preproc</span><span class="sxs-lookup"><span data-stu-id="cea68-121">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC</span></span>](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [<span data-ttu-id="cea68-122">\_relleno de \_ \_ ruido \_ de MFPKEY WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="cea68-122">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL</span></span>](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [<span data-ttu-id="cea68-123">MFPKEY \_ WMAAECMA \_ feat \_</span><span class="sxs-lookup"><span data-stu-id="cea68-123">MFPKEY\_WMAAECMA\_FEATR\_NS</span></span>](mfpkey-wmaaecma-featr-nsproperty.md)
-   [<span data-ttu-id="cea68-124">MFPKEY \_ WMAAECMA \_ feat \_ VAD</span><span class="sxs-lookup"><span data-stu-id="cea68-124">MFPKEY\_WMAAECMA\_FEATR\_VAD</span></span>](mfpkey-wmaaecma-featr-vadproperty.md)

<span data-ttu-id="cea68-125">Si esta propiedad es VARIANT \_ false, el DSP omite estas propiedades y usa su configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="cea68-125">If this property is VARIANT\_FALSE, the DSP ignores these properties and uses its default settings.</span></span> <span data-ttu-id="cea68-126">El valor predeterminado de esta propiedad es VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="cea68-126">The default value of this property is VARIANT\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea68-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cea68-127">Requirements</span></span>



| <span data-ttu-id="cea68-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cea68-128">Requirement</span></span> | <span data-ttu-id="cea68-129">Value</span><span class="sxs-lookup"><span data-stu-id="cea68-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cea68-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cea68-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cea68-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cea68-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cea68-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cea68-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cea68-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cea68-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cea68-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cea68-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="cea68-135"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cea68-135"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cea68-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="cea68-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea68-137">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cea68-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="cea68-138">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="cea68-138">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
