---
description: Identifica la combinación de dispositivos de audio que la aplicación está usando actualmente con el DSP de captura de voz.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: Propiedad MFPKEY_WMAAECMA_DEVICEPAIR_GUID (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a586d7d31f29b20eb7ca39320d5fa57b9943715a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155392"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a><span data-ttu-id="2dddf-103">MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID</span><span class="sxs-lookup"><span data-stu-id="2dddf-103">MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID Property</span></span>

<span data-ttu-id="2dddf-104">Identifica la combinación de dispositivos de audio que la aplicación está usando actualmente con el DSP de captura de voz.</span><span class="sxs-lookup"><span data-stu-id="2dddf-104">Identifies the combination of audio devices that the application is currently using with the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2dddf-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2dddf-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2dddf-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="2dddf-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2dddf-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="2dddf-107">Data Type</span></span>

<span data-ttu-id="2dddf-108">VT \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="2dddf-108">VT\_CLSID</span></span>

## <a name="applies-to"></a><span data-ttu-id="2dddf-109">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="2dddf-109">Applies To</span></span>

-   [<span data-ttu-id="2dddf-110">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="2dddf-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="2dddf-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dddf-111">Remarks</span></span>

<span data-ttu-id="2dddf-112">Establezca esta propiedad si usa el DSP en modo de filtro y el valor de la propiedad [MFPKEY \_ WMAAECMA \_ recuperar \_ \_ estadísticas de TS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) es Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="2dddf-112">Set this property if you are using the DSP in filter mode and the value of the [MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE.</span></span>

<span data-ttu-id="2dddf-113">Cuando la propiedad [**MFPKEY \_ WMAAECMA \_ Retrieve \_ TS \_ stats**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) es Variant \_ true, el DSP recopila estadísticas sobre las marcas de tiempo de los dispositivos de audio y almacena esta información en el registro.</span><span class="sxs-lookup"><span data-stu-id="2dddf-113">When the [**MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE, the DSP collects statistics about the time stamps from the audio devices and stores this information in the registry.</span></span> <span data-ttu-id="2dddf-114">Estas estadísticas pueden cambiar para cada combinación de dispositivo de captura de audio y dispositivo de representación de audio.</span><span class="sxs-lookup"><span data-stu-id="2dddf-114">These statistics can change for each combination of audio capture device and audio rendering device.</span></span> <span data-ttu-id="2dddf-115">Por lo tanto, la aplicación debe asignar un GUID para identificar la combinación determinada de dispositivos en uso.</span><span class="sxs-lookup"><span data-stu-id="2dddf-115">Therefore, the application must assign a GUID to identify the particular combination of devices in use.</span></span> <span data-ttu-id="2dddf-116">La aplicación debe realizar un seguimiento de este GUID para que pueda asignar el mismo GUID siempre que use el mismo par de dispositivos de audio.</span><span class="sxs-lookup"><span data-stu-id="2dddf-116">The application should keep track of this GUID, so that it can assign the same GUID whenever it uses the same pair of audio devices.</span></span>

<span data-ttu-id="2dddf-117">Si usa el DSP en modo de origen, no es necesario establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2dddf-117">If you are using the DSP in source mode, you do not need to set this property.</span></span> <span data-ttu-id="2dddf-118">El DSP genera automáticamente un GUID basado en el valor de la propiedad [MFPKEY \_ WMAAECMA \_ Device \_ Indexes](mfpkey-wmaaecma-device-indexesproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="2dddf-118">The DSP automatically generates a GUID based on the value of the [MFPKEY\_WMAAECMA\_DEVICE\_INDEXES](mfpkey-wmaaecma-device-indexesproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dddf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dddf-119">Requirements</span></span>



| <span data-ttu-id="2dddf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dddf-120">Requirement</span></span> | <span data-ttu-id="2dddf-121">Value</span><span class="sxs-lookup"><span data-stu-id="2dddf-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dddf-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dddf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2dddf-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2dddf-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2dddf-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2dddf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2dddf-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2dddf-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2dddf-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2dddf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dddf-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dddf-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dddf-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dddf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dddf-129">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2dddf-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2dddf-130">DSP de captura de voz</span><span class="sxs-lookup"><span data-stu-id="2dddf-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
