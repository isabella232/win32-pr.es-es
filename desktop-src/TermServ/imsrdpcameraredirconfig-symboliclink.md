---
title: Propiedad SymbolicLink de la interfaz IMsRdpCameraRedirConfig
description: Obtiene el vínculo simbólico de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad SymbolicLink
- Propiedad SymbolicLink Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfig
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfig, propiedad SymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "103906287"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a><span data-ttu-id="4da97-106">IMsRdpCameraRedirConfig:: SymbolicLink (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4da97-106">IMsRdpCameraRedirConfig::SymbolicLink property</span></span>

<span data-ttu-id="4da97-107">Obtiene el vínculo simbólico de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.</span><span class="sxs-lookup"><span data-stu-id="4da97-107">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="4da97-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4da97-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da97-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4da97-109">Syntax</span></span>

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a><span data-ttu-id="4da97-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4da97-110">Property value</span></span>

<span data-ttu-id="4da97-111">Vínculo simbólico de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.</span><span class="sxs-lookup"><span data-stu-id="4da97-111">The symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da97-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4da97-112">Requirements</span></span>

| <span data-ttu-id="4da97-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4da97-113">Requirement</span></span> | <span data-ttu-id="4da97-114">Value</span><span class="sxs-lookup"><span data-stu-id="4da97-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="4da97-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4da97-115">Minimum supported client</span></span>| <span data-ttu-id="4da97-116">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="4da97-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="4da97-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4da97-117">Type library</span></span>            | <span data-ttu-id="4da97-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="4da97-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="4da97-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4da97-119">DLL</span></span>                  | <span data-ttu-id="4da97-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="4da97-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="4da97-121">IID</span><span class="sxs-lookup"><span data-stu-id="4da97-121">IID</span></span>                      | <span data-ttu-id="4da97-122">IID \_ IMsRdpCameraRedirConfig se define como 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="4da97-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="4da97-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4da97-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da97-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="4da97-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>