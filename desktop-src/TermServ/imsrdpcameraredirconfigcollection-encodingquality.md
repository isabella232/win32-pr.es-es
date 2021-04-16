---
title: Propiedad EncodingQuality de la interfaz IMsRdpCameraRedirConfigCollection
description: Especifica la calidad de codificación (velocidad de bits).
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad EncodingQuality
- Propiedad EncodingQuality Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfigCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection, propiedad EncodingQuality
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d8044c2fb70233243a3a74d8dc5faac96873cb48
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494158"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a><span data-ttu-id="77f8b-106">IMsRdpCameraRedirConfigCollection:: EncodingQuality (propiedad)</span><span class="sxs-lookup"><span data-stu-id="77f8b-106">IMsRdpCameraRedirConfigCollection::EncodingQuality property</span></span>

<span data-ttu-id="77f8b-107">Especifica la calidad de codificación (velocidad de bits).</span><span class="sxs-lookup"><span data-stu-id="77f8b-107">Specifies the encoding quality (bit rate).</span></span>

<span data-ttu-id="77f8b-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="77f8b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="77f8b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77f8b-109">Syntax</span></span>

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a><span data-ttu-id="77f8b-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="77f8b-110">Property value</span></span>

<span data-ttu-id="77f8b-111">Uno de los siguientes valores de enumeración de **CameraRedirEncodingQuality** que especifica la calidad de codificación (velocidad de bits).</span><span class="sxs-lookup"><span data-stu-id="77f8b-111">One of the following **CameraRedirEncodingQuality** enum values that specifies the encoding quality (bit rate).</span></span>

| <span data-ttu-id="77f8b-112">Nombre del miembro de enumeración</span><span class="sxs-lookup"><span data-stu-id="77f8b-112">Enum member name</span></span> | <span data-ttu-id="77f8b-113">Value</span><span class="sxs-lookup"><span data-stu-id="77f8b-113">Value</span></span> |
|-----------------|--------|
| <span data-ttu-id="77f8b-114">encodingQualityLow</span><span class="sxs-lookup"><span data-stu-id="77f8b-114">encodingQualityLow</span></span> | <span data-ttu-id="77f8b-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="77f8b-115">0x0000</span></span> |
| <span data-ttu-id="77f8b-116">encodingQualityMedium</span><span class="sxs-lookup"><span data-stu-id="77f8b-116">encodingQualityMedium</span></span> | <span data-ttu-id="77f8b-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="77f8b-117">0x0001</span></span> |
| <span data-ttu-id="77f8b-118">encodingQualityHigh</span><span class="sxs-lookup"><span data-stu-id="77f8b-118">encodingQualityHigh</span></span> | <span data-ttu-id="77f8b-119">0x0002</span><span class="sxs-lookup"><span data-stu-id="77f8b-119">0x0002</span></span> |

## <a name="requirements"></a><span data-ttu-id="77f8b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77f8b-120">Requirements</span></span>

| <span data-ttu-id="77f8b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="77f8b-121">Requirement</span></span> | <span data-ttu-id="77f8b-122">Value</span><span class="sxs-lookup"><span data-stu-id="77f8b-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="77f8b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77f8b-123">Minimum supported client</span></span>| <span data-ttu-id="77f8b-124">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="77f8b-124">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="77f8b-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="77f8b-125">Type library</span></span>            | <span data-ttu-id="77f8b-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="77f8b-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="77f8b-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="77f8b-127">DLL</span></span>                  | <span data-ttu-id="77f8b-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="77f8b-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="77f8b-129">IID</span><span class="sxs-lookup"><span data-stu-id="77f8b-129">IID</span></span>                      | <span data-ttu-id="77f8b-130">IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="77f8b-130">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="77f8b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="77f8b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f8b-132">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="77f8b-132">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>