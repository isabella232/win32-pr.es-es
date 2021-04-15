---
title: Propiedad DeviceExists de la interfaz IMsRdpCameraRedirConfig
description: Especifica si el dispositivo de cámara existe actualmente (es decir, si la cámara está conectada).
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DeviceExists
- Propiedad DeviceExists Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfig
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfig, propiedad DeviceExists
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 368b2d46e6dfc2c32c0bb294edceda31f8a58f4e
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494176"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a><span data-ttu-id="49e20-106">IMsRdpCameraRedirConfig::D propiedad eviceExists</span><span class="sxs-lookup"><span data-stu-id="49e20-106">IMsRdpCameraRedirConfig::DeviceExists property</span></span>

<span data-ttu-id="49e20-107">Especifica si el dispositivo de cámara existe actualmente (es decir, si la cámara está conectada).</span><span class="sxs-lookup"><span data-stu-id="49e20-107">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>

<span data-ttu-id="49e20-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="49e20-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e20-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49e20-109">Syntax</span></span>

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a><span data-ttu-id="49e20-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="49e20-110">Property value</span></span>

<span data-ttu-id="49e20-111">Valor que indica si el dispositivo de cámara existe actualmente (es decir, si la cámara está conectada).</span><span class="sxs-lookup"><span data-stu-id="49e20-111">A value that indicates whether or not the camera device currently exists (that is, the camera is connected).</span></span>

## <a name="requirements"></a><span data-ttu-id="49e20-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49e20-112">Requirements</span></span>

| <span data-ttu-id="49e20-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="49e20-113">Requirement</span></span> | <span data-ttu-id="49e20-114">Value</span><span class="sxs-lookup"><span data-stu-id="49e20-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="49e20-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49e20-115">Minimum supported client</span></span>| <span data-ttu-id="49e20-116">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="49e20-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="49e20-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="49e20-117">Type library</span></span>            | <span data-ttu-id="49e20-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="49e20-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="49e20-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49e20-119">DLL</span></span>                  | <span data-ttu-id="49e20-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="49e20-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="49e20-121">IID</span><span class="sxs-lookup"><span data-stu-id="49e20-121">IID</span></span>                      | <span data-ttu-id="49e20-122">IID \_ IMsRdpCameraRedirConfig se define como 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="49e20-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="49e20-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="49e20-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e20-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="49e20-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>