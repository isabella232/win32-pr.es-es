---
description: Especifica la duración del eco que el algoritmo de cancelación del eco acústico (AEC) puede controlar, en milisegundos.
ms.assetid: d451b90f-7ef7-4f66-be83-aca93e3ad894
title: Propiedad MFPKEY_WMAAECMA_FEATR_ECHO_LENGTH (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d66f7dcc4764447495e0f3ae55d2d038c2a8d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696698"
---
# <a name="mfpkey_wmaaecma_featr_echo_length-property"></a><span data-ttu-id="0aa4f-103">\_Propiedad de \_ longitud de \_ eco \_ del MFPKEY de WMAAECMA</span><span class="sxs-lookup"><span data-stu-id="0aa4f-103">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH Property</span></span>

<span data-ttu-id="0aa4f-104">Especifica la duración del eco que el algoritmo de cancelación del eco acústico (AEC) puede controlar, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-104">Specifies the duration of echo that the acoustic echo cancellation (AEC) algorithm can handle, in milliseconds.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0aa4f-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0aa4f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0aa4f-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="0aa4f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="0aa4f-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0aa4f-107">Data Type</span></span>

<span data-ttu-id="0aa4f-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="0aa4f-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="0aa4f-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0aa4f-109">Default Value</span></span>

<span data-ttu-id="0aa4f-110">256</span><span class="sxs-lookup"><span data-stu-id="0aa4f-110">256</span></span>

## <a name="applies-to"></a><span data-ttu-id="0aa4f-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="0aa4f-111">Applies To</span></span>

-   [<span data-ttu-id="0aa4f-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="0aa4f-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="0aa4f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0aa4f-113">Remarks</span></span>

<span data-ttu-id="0aa4f-114">El algoritmo AEC usa un filtro adaptable cuya longitud viene determinada por la duración del eco.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-114">The AEC algorithm uses an adaptive filter whose length is determined by the duration of the echo.</span></span> <span data-ttu-id="0aa4f-115">Se recomienda que las aplicaciones usen uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="0aa4f-115">It is recommended that applications use one of the following values:</span></span>

-   <span data-ttu-id="0aa4f-116">128</span><span class="sxs-lookup"><span data-stu-id="0aa4f-116">128</span></span>
-   <span data-ttu-id="0aa4f-117">256</span><span class="sxs-lookup"><span data-stu-id="0aa4f-117">256</span></span>
-   <span data-ttu-id="0aa4f-118">512</span><span class="sxs-lookup"><span data-stu-id="0aa4f-118">512</span></span>
-   <span data-ttu-id="0aa4f-119">1024</span><span class="sxs-lookup"><span data-stu-id="0aa4f-119">1024</span></span>

<span data-ttu-id="0aa4f-120">El valor predeterminado es 256 milisegundos, que es suficiente para la mayoría de los entornos de oficina y de casa.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-120">The default value is 256 milliseconds, which is sufficient for most office and home environments.</span></span> <span data-ttu-id="0aa4f-121">Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="0aa4f-122">El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0aa4f-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa4f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aa4f-123">Requirements</span></span>



| <span data-ttu-id="0aa4f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa4f-124">Requirement</span></span> | <span data-ttu-id="0aa4f-125">Value</span><span class="sxs-lookup"><span data-stu-id="0aa4f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa4f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0aa4f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa4f-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0aa4f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0aa4f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0aa4f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa4f-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0aa4f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0aa4f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0aa4f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa4f-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aa4f-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aa4f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0aa4f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa4f-133">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0aa4f-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="0aa4f-134">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="0aa4f-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
