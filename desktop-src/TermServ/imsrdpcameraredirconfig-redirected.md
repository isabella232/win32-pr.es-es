---
title: Propiedad Redirected de la interfaz IMsRdpCameraRedirConfig
description: Especifica si se redirige la cámara.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de propiedad redirigida
- Servicios de Escritorio remoto de propiedad redirigida, interfaz IMsRdpCameraRedirConfig
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfig, propiedad redirigida
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.Redirected
- IMsRdpCameraRedirConfig.put_Redirected
- IMsRdpCameraRedirConfig.get_Redirected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: f81dc643f7911029df088bbb692d7c8c06fddac4
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494170"
---
# <a name="imsrdpcameraredirconfigredirected-property"></a><span data-ttu-id="c343b-106">IMsRdpCameraRedirConfig:: redirigiód (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c343b-106">IMsRdpCameraRedirConfig::Redirected property</span></span>

<span data-ttu-id="c343b-107">Especifica si se redirige la cámara.</span><span class="sxs-lookup"><span data-stu-id="c343b-107">Specifies whether or not the camera is redirected.</span></span>

<span data-ttu-id="c343b-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c343b-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c343b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c343b-109">Syntax</span></span>

```C++
HRESULT put_Redirected(
    [in] VARIANT_BOOL fRedirected
);

HRESULT get_Redirected(
    [out, retval] VARIANT_BOOL* pfRedirected
);
```

## <a name="property-value"></a><span data-ttu-id="c343b-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c343b-110">Property value</span></span>

<span data-ttu-id="c343b-111">Valor que especifica si se redirige la cámara.</span><span class="sxs-lookup"><span data-stu-id="c343b-111">A value that specifies whether or not the camera is redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="c343b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c343b-112">Requirements</span></span>

| <span data-ttu-id="c343b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c343b-113">Requirement</span></span> | <span data-ttu-id="c343b-114">Value</span><span class="sxs-lookup"><span data-stu-id="c343b-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="c343b-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c343b-115">Minimum supported client</span></span>| <span data-ttu-id="c343b-116">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="c343b-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="c343b-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c343b-117">Type library</span></span>            | <span data-ttu-id="c343b-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c343b-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="c343b-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c343b-119">DLL</span></span>                  | <span data-ttu-id="c343b-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c343b-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="c343b-121">IID</span><span class="sxs-lookup"><span data-stu-id="c343b-121">IID</span></span>                      | <span data-ttu-id="c343b-122">IID \_ IMsRdpCameraRedirConfig se define como 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="c343b-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="c343b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c343b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c343b-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="c343b-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>