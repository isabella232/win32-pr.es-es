---
title: Propiedad Clipboard de la interfaz IMsRdpClientNonScriptable7
description: Obtiene el controlador del portapapeles que se usa para sincronizar los portapapeles locales y remotos si está habilitada la sincronización manual del portapapeles.
ms.tgt_platform: multiple
keywords:
- Propiedad Clipboard Servicios de Escritorio remoto
- Propiedad Clipboard Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable7, propiedad Clipboard
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.Clipboard
- IMsRdpClientNonScriptable7.get_Clipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 770930eb780b3ce8684608ffcdc0c13c1630cab0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "103997613"
---
# <a name="imsrdpclientnonscriptable7clipboard-property"></a><span data-ttu-id="60cda-106">IMsRdpClientNonScriptable7:: Clipboard (propiedad)</span><span class="sxs-lookup"><span data-stu-id="60cda-106">IMsRdpClientNonScriptable7::Clipboard property</span></span>

<span data-ttu-id="60cda-107">Obtiene el controlador del portapapeles que se usa para sincronizar los portapapeles locales y remotos si está habilitada la sincronización manual del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="60cda-107">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>

<span data-ttu-id="60cda-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="60cda-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="60cda-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60cda-109">Syntax</span></span>

```C++
HRESULT get_Clipboard(
  [out, retval] IMsRdpClipboard** ppClipboard
);
```

## <a name="property-value"></a><span data-ttu-id="60cda-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="60cda-110">Property value</span></span>

<span data-ttu-id="60cda-111">Un [IMsRdpClipboard](imsrdpclipboard.md) que representa el controlador del portapapeles que se usa para sincronizar los portapapeles locales y remotos si está habilitada la sincronización manual del portapapeles (es decir, el valor de la propiedad [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) se establece en **true**).</span><span class="sxs-lookup"><span data-stu-id="60cda-111">An [IMsRdpClipboard](imsrdpclipboard.md) that represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="requirements"></a><span data-ttu-id="60cda-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60cda-112">Requirements</span></span>

| <span data-ttu-id="60cda-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="60cda-113">Requirement</span></span> | <span data-ttu-id="60cda-114">Value</span><span class="sxs-lookup"><span data-stu-id="60cda-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="60cda-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60cda-115">Minimum supported client</span></span>| <span data-ttu-id="60cda-116">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="60cda-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="60cda-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="60cda-117">Type library</span></span>            | <span data-ttu-id="60cda-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="60cda-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="60cda-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60cda-119">DLL</span></span>                  | <span data-ttu-id="60cda-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="60cda-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="60cda-121">IID</span><span class="sxs-lookup"><span data-stu-id="60cda-121">IID</span></span>                      | <span data-ttu-id="60cda-122">IID \_ IMsRdpClientNonScriptable7 se define como 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="60cda-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="60cda-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="60cda-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60cda-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="60cda-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>