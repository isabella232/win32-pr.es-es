---
title: Propiedad ParentInstanceId de la interfaz IMsRdpCameraRedirConfig
description: Obtiene el identificador de instancia del dispositivo primario de la cámara.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ParentInstanceId
- Propiedad ParentInstanceId Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfig
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfig, propiedad ParentInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e4a399659c33000207930bfe7d17818a2ad8438f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "105720246"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a><span data-ttu-id="4b6e6-106">IMsRdpCameraRedirConfig::P propiedad arentInstanceId</span><span class="sxs-lookup"><span data-stu-id="4b6e6-106">IMsRdpCameraRedirConfig::ParentInstanceId property</span></span>

<span data-ttu-id="4b6e6-107">Obtiene el identificador de instancia del dispositivo primario de la cámara.</span><span class="sxs-lookup"><span data-stu-id="4b6e6-107">Gets the parent device instance ID of the camera.</span></span>

<span data-ttu-id="4b6e6-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4b6e6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b6e6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b6e6-109">Syntax</span></span>

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a><span data-ttu-id="4b6e6-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4b6e6-110">Property value</span></span>

<span data-ttu-id="4b6e6-111">IDENTIFICADOR de instancia del dispositivo primario de la cámara.</span><span class="sxs-lookup"><span data-stu-id="4b6e6-111">The parent device instance ID of the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b6e6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b6e6-112">Requirements</span></span>

| <span data-ttu-id="4b6e6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b6e6-113">Requirement</span></span> | <span data-ttu-id="4b6e6-114">Value</span><span class="sxs-lookup"><span data-stu-id="4b6e6-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="4b6e6-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b6e6-115">Minimum supported client</span></span>| <span data-ttu-id="4b6e6-116">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="4b6e6-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="4b6e6-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4b6e6-117">Type library</span></span>            | <span data-ttu-id="4b6e6-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="4b6e6-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="4b6e6-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b6e6-119">DLL</span></span>                  | <span data-ttu-id="4b6e6-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="4b6e6-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="4b6e6-121">IID</span><span class="sxs-lookup"><span data-stu-id="4b6e6-121">IID</span></span>                      | <span data-ttu-id="4b6e6-122">IID \_ IMsRdpCameraRedirConfig se define como 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="4b6e6-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="4b6e6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b6e6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b6e6-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="4b6e6-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>