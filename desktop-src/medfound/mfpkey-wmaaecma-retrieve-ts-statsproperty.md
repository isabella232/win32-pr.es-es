---
description: Especifica si el DSP de la captura de voz almacena las estadísticas de la marca de tiempo en el registro.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: Propiedad MFPKEY_WMAAECMA_RETRIEVE_TS_STATS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696690"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a><span data-ttu-id="2ee29-103">MFPKEY \_ WMAAECMA \_ recuperar \_ la \_ propiedad de estadísticas de TS</span><span class="sxs-lookup"><span data-stu-id="2ee29-103">MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS Property</span></span>

<span data-ttu-id="2ee29-104">Especifica si el DSP de la captura de voz almacena las estadísticas de la marca de tiempo en el registro.</span><span class="sxs-lookup"><span data-stu-id="2ee29-104">Specifies whether the Voice Capture DSP stores time stamp statistics in the registry.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2ee29-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2ee29-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2ee29-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="2ee29-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2ee29-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2ee29-107">Data Type</span></span>

<span data-ttu-id="2ee29-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="2ee29-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="2ee29-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2ee29-109">Default Value</span></span>

<span data-ttu-id="2ee29-110">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="2ee29-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="2ee29-111">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="2ee29-111">Applies To</span></span>

-   [<span data-ttu-id="2ee29-112">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="2ee29-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="2ee29-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ee29-113">Remarks</span></span>

<span data-ttu-id="2ee29-114">Los algoritmos de cancelación del eco acústico (AEC) dependen de las marcas de tiempo precisas en las secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="2ee29-114">Acoustic echo cancellation (AEC) algorithms depend on accurate time stamps on the audio streams.</span></span> <span data-ttu-id="2ee29-115">En realidad, las marcas de tiempo suelen ser imperfectas y los distintos dispositivos de audio pueden presentar diferentes tasas de varianza y de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="2ee29-115">In reality, time stamps are often imperfect, and different audio devices can exhibit different rates of variance and drift.</span></span> <span data-ttu-id="2ee29-116">Cuando AEC está habilitado, el DSP recopila estadísticas sobre las marcas de tiempo y usa esta información para compensar las imprecisiones.</span><span class="sxs-lookup"><span data-stu-id="2ee29-116">When AEC is enabled, the DSP collects statistics about the time stamps and uses this information to compensate for inaccuracies.</span></span>

<span data-ttu-id="2ee29-117">Si el valor de esta propiedad es VARIANT \_ true, el DSP guarda las estadísticas que recopila en el registro.</span><span class="sxs-lookup"><span data-stu-id="2ee29-117">If the value of this property is VARIANT\_TRUE, the DSP saves the statistics that it collects in the registry.</span></span> <span data-ttu-id="2ee29-118">La próxima vez que el DSP realice el AEC usando el mismo par de dispositivos de audio, leerá la información estadística del registro, lo que permite que el DSP funcione de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="2ee29-118">The next time the DSP performs AEC using the same pair of audio devices, it reads the statistical information from the registry, which enables the DSP to perform more efficiently.</span></span>

<span data-ttu-id="2ee29-119">Si establece el valor de esta propiedad en VARIANT \_ true y usa el DSP en modo de filtro, también debe establecer la propiedad [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="2ee29-119">If you set the value of this property to VARIANT\_TRUE and you are using the DSP in filter mode, you should also set the [MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) property.</span></span> <span data-ttu-id="2ee29-120">En el modo de origen, esto no es necesario.</span><span class="sxs-lookup"><span data-stu-id="2ee29-120">In source mode, this is not required.</span></span>

<span data-ttu-id="2ee29-121">El valor predeterminado de esta propiedad es VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="2ee29-121">The default value of this property is VARIANT\_FALSE.</span></span> <span data-ttu-id="2ee29-122">El DSP usa esta propiedad solo cuando el procesamiento de AEC está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2ee29-122">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ee29-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ee29-123">Requirements</span></span>



| <span data-ttu-id="2ee29-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ee29-124">Requirement</span></span> | <span data-ttu-id="2ee29-125">Value</span><span class="sxs-lookup"><span data-stu-id="2ee29-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee29-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ee29-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee29-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2ee29-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2ee29-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ee29-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee29-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ee29-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ee29-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ee29-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ee29-131"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ee29-131"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ee29-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ee29-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee29-133">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2ee29-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2ee29-134">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="2ee29-134">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
