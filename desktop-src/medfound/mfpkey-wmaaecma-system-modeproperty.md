---
description: Establece el modo de procesamiento del DSP de la captura de voz.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: Propiedad MFPKEY_WMAAECMA_SYSTEM_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666875"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a><span data-ttu-id="12095-103">\_Propiedad de \_ modo de sistema de MFPKEY WMAAECMA \_</span><span class="sxs-lookup"><span data-stu-id="12095-103">MFPKEY\_WMAAECMA\_SYSTEM\_MODE Property</span></span>

<span data-ttu-id="12095-104">Establece el modo de procesamiento del DSP de la captura de voz.</span><span class="sxs-lookup"><span data-stu-id="12095-104">Sets the processing mode for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="12095-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="12095-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="12095-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="12095-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="12095-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="12095-107">Data Type</span></span>

<span data-ttu-id="12095-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="12095-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="12095-109">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="12095-109">Applies To</span></span>

-   [<span data-ttu-id="12095-110">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="12095-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="12095-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12095-111">Remarks</span></span>

<span data-ttu-id="12095-112">El valor de esta propiedad es un miembro de la enumeración del [ \_ \_ modo del sistema AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .</span><span class="sxs-lookup"><span data-stu-id="12095-112">The value of this property is a member of the [AEC\_SYSTEM\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) enumeration.</span></span>

<span data-ttu-id="12095-113">La propiedad debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="12095-113">The property must be one of the following values.</span></span>



| <span data-ttu-id="12095-114">Value</span><span class="sxs-lookup"><span data-stu-id="12095-114">Value</span></span> | <span data-ttu-id="12095-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="12095-115">Description</span></span>                                 |
|-------|---------------------------------------------|
| <span data-ttu-id="12095-116">0</span><span class="sxs-lookup"><span data-stu-id="12095-116">0</span></span>     | <span data-ttu-id="12095-117">Modo solo de cancelación de eco de audio (AEC)</span><span class="sxs-lookup"><span data-stu-id="12095-117">Audio echo cancellation (AEC) only mode</span></span>     |
| <span data-ttu-id="12095-118">2</span><span class="sxs-lookup"><span data-stu-id="12095-118">2</span></span>     | <span data-ttu-id="12095-119">Modo solo de procesamiento de matriz de micrófono (mapa)</span><span class="sxs-lookup"><span data-stu-id="12095-119">Microphone array processing (MAP) only mode</span></span> |
| <span data-ttu-id="12095-120">4</span><span class="sxs-lookup"><span data-stu-id="12095-120">4</span></span>     | <span data-ttu-id="12095-121">AEC y modo de mapa</span><span class="sxs-lookup"><span data-stu-id="12095-121">AEC and MAP mode</span></span>                            |
| <span data-ttu-id="12095-122">5</span><span class="sxs-lookup"><span data-stu-id="12095-122">5</span></span>     | <span data-ttu-id="12095-123">Ni AEC ni el modo de asignación</span><span class="sxs-lookup"><span data-stu-id="12095-123">Neither AEC nor MAP mode</span></span>                    |



 

<span data-ttu-id="12095-124">Debe establecer esta propiedad antes de usar el DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="12095-124">You must set this property before using the Voice Capture DSP.</span></span> <span data-ttu-id="12095-125">Después de establecer esta propiedad, puede usar el DSP con su configuración predeterminada o establecer propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="12095-125">After you set this property, you can use the DSP with its default settings, or set additional properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="12095-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12095-126">Requirements</span></span>



| <span data-ttu-id="12095-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="12095-127">Requirement</span></span> | <span data-ttu-id="12095-128">Value</span><span class="sxs-lookup"><span data-stu-id="12095-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12095-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12095-129">Minimum supported client</span></span><br/> | <span data-ttu-id="12095-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="12095-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="12095-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12095-131">Minimum supported server</span></span><br/> | <span data-ttu-id="12095-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="12095-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12095-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12095-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="12095-134"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="12095-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12095-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="12095-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12095-136">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12095-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="12095-137">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="12095-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
