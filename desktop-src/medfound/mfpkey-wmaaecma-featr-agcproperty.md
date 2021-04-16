---
description: Especifica si el DSP de la captura de voz realiza el control automático de ganancia.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: Propiedad MFPKEY_WMAAECMA_FEATR_AGC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696699"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a><span data-ttu-id="12246-103">\_Propiedad AGC del MFPKEY WMAAECMA \_ feat \_</span><span class="sxs-lookup"><span data-stu-id="12246-103">MFPKEY\_WMAAECMA\_FEATR\_AGC Property</span></span>

<span data-ttu-id="12246-104">Especifica si el DSP de la captura de voz realiza el control automático de ganancia.</span><span class="sxs-lookup"><span data-stu-id="12246-104">Specifies whether the Voice Capture DSP performs automatic gain control.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="12246-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="12246-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="12246-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="12246-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="12246-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="12246-107">Data Type</span></span>

<span data-ttu-id="12246-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="12246-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="12246-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="12246-109">Default Value</span></span>

<span data-ttu-id="12246-110">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="12246-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="12246-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="12246-111">Applies To</span></span>

-   [<span data-ttu-id="12246-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="12246-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="12246-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12246-113">Remarks</span></span>

<span data-ttu-id="12246-114">El control de ganancia automática es un componente de procesamiento de señal digital (DSP) que ajusta la ganancia para que el nivel de salida de la señal permanezca dentro del mismo intervalo aproximado.</span><span class="sxs-lookup"><span data-stu-id="12246-114">Automatic gain control is a digital signal processing (DSP) component that adjusts the gain so that the output level of the signal remains within the same approximate range.</span></span>

<span data-ttu-id="12246-115">Esta propiedad puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="12246-115">This property can have the following values.</span></span>



| <span data-ttu-id="12246-116">Value</span><span class="sxs-lookup"><span data-stu-id="12246-116">Value</span></span>          | <span data-ttu-id="12246-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="12246-117">Description</span></span>                     |
|----------------|---------------------------------|
| <span data-ttu-id="12246-118">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="12246-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="12246-119">Deshabilitar el control de ganancia automática.</span><span class="sxs-lookup"><span data-stu-id="12246-119">Disable automatic gain control.</span></span> |
| <span data-ttu-id="12246-120">VARIANTE \_ true</span><span class="sxs-lookup"><span data-stu-id="12246-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="12246-121">Habilitar el control de ganancia automática.</span><span class="sxs-lookup"><span data-stu-id="12246-121">Enable automatic gain control.</span></span>  |



 

<span data-ttu-id="12246-122">El valor predeterminado de esta propiedad es VARIANT \_ false (disabled).</span><span class="sxs-lookup"><span data-stu-id="12246-122">The default value of this property is VARIANT\_FALSE (disabled).</span></span> <span data-ttu-id="12246-123">Antes de establecer esta propiedad, debe establecer la propiedad de [ \_ modo de \_ característica \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) en Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="12246-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="12246-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12246-124">Requirements</span></span>



| <span data-ttu-id="12246-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="12246-125">Requirement</span></span> | <span data-ttu-id="12246-126">Value</span><span class="sxs-lookup"><span data-stu-id="12246-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12246-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12246-127">Minimum supported client</span></span><br/> | <span data-ttu-id="12246-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="12246-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="12246-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12246-129">Minimum supported server</span></span><br/> | <span data-ttu-id="12246-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="12246-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12246-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12246-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="12246-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="12246-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12246-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="12246-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12246-134">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12246-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="12246-135">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="12246-135">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
