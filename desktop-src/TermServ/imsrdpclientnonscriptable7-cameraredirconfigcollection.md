---
title: Propiedad CameraRedirConfigCollection de la interfaz IMsRdpClientNonScriptable7
description: Obtiene la colección de cámaras (y las configuraciones asociadas) que están disponibles para la redirección.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad CameraRedirConfigCollection
- Propiedad CameraRedirConfigCollection Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable7, propiedad CameraRedirConfigCollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104359878"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a><span data-ttu-id="9e327-106">IMsRdpClientNonScriptable7:: CameraRedirConfigCollection (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9e327-106">IMsRdpClientNonScriptable7::CameraRedirConfigCollection property</span></span>

<span data-ttu-id="9e327-107">Obtiene la colección de cámaras (y las configuraciones asociadas) que están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="9e327-107">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

<span data-ttu-id="9e327-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9e327-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e327-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e327-109">Syntax</span></span>


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a><span data-ttu-id="9e327-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9e327-110">Property value</span></span>

<span data-ttu-id="9e327-111">Un [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) que representa la colección de cámaras (y las configuraciones asociadas) que están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="9e327-111">An [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) that represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e327-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e327-112">Requirements</span></span>

| <span data-ttu-id="9e327-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e327-113">Requirement</span></span> | <span data-ttu-id="9e327-114">Value</span><span class="sxs-lookup"><span data-stu-id="9e327-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="9e327-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e327-115">Minimum supported client</span></span>| <span data-ttu-id="9e327-116">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="9e327-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="9e327-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9e327-117">Type library</span></span>            | <span data-ttu-id="9e327-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9e327-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="9e327-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e327-119">DLL</span></span>                  | <span data-ttu-id="9e327-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9e327-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="9e327-121">IID</span><span class="sxs-lookup"><span data-stu-id="9e327-121">IID</span></span>                      | <span data-ttu-id="9e327-122">IID \_ IMsRdpClientNonScriptable7 se define como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="9e327-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="9e327-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e327-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e327-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="9e327-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>