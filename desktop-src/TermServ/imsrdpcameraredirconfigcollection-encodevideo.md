---
title: Propiedad EncodeVideo de la interfaz IMsRdpCameraRedirConfigCollection
description: Especifica si la secuencia de vídeo es H. 264 codificada.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad EncodeVideo
- Propiedad EncodeVideo Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfigCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection, propiedad EncodeVideo
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 6b2994f4db3de04f339bb242120b6c63cd2e0c7b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104151925"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a><span data-ttu-id="b2bf0-106">IMsRdpCameraRedirConfigCollection:: EncodeVideo (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b2bf0-106">IMsRdpCameraRedirConfigCollection::EncodeVideo property</span></span>

<span data-ttu-id="b2bf0-107">Especifica si la secuencia de vídeo es H. 264 codificada.</span><span class="sxs-lookup"><span data-stu-id="b2bf0-107">Specifies whether or not the video stream is H.264 encoded.</span></span>

<span data-ttu-id="b2bf0-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b2bf0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2bf0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2bf0-109">Syntax</span></span>

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a><span data-ttu-id="b2bf0-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b2bf0-110">Property value</span></span>

<span data-ttu-id="b2bf0-111">Valor que indica si la secuencia de vídeo es H. 264 codificada.</span><span class="sxs-lookup"><span data-stu-id="b2bf0-111">A value that indicates whether or not the video stream is H.264 encoded.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2bf0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2bf0-112">Requirements</span></span>

| <span data-ttu-id="b2bf0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2bf0-113">Requirement</span></span> | <span data-ttu-id="b2bf0-114">Value</span><span class="sxs-lookup"><span data-stu-id="b2bf0-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="b2bf0-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2bf0-115">Minimum supported client</span></span>| <span data-ttu-id="b2bf0-116">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="b2bf0-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="b2bf0-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b2bf0-117">Type library</span></span>            | <span data-ttu-id="b2bf0-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b2bf0-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="b2bf0-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2bf0-119">DLL</span></span>                  | <span data-ttu-id="b2bf0-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b2bf0-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="b2bf0-121">IID</span><span class="sxs-lookup"><span data-stu-id="b2bf0-121">IID</span></span>                      | <span data-ttu-id="b2bf0-122">IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="b2bf0-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="b2bf0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2bf0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2bf0-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="b2bf0-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>