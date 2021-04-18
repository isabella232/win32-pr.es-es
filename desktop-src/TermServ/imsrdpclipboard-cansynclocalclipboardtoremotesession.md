---
title: Método CanSyncLocalClipboardToRemoteSession de la interfaz IMsRdpClipboard
description: Indica si el portapapeles local se puede sincronizar con la sesión remota.
ms.tgt_platform: multiple
keywords:
- Método CanSyncLocalClipboardToRemoteSession Servicios de Escritorio remoto
- Método CanSyncLocalClipboardToRemoteSession Servicios de Escritorio remoto, interfaz IMsRdpClipboard
- Interfaz IMsRdpClipboard Servicios de Escritorio remoto, método CanSyncLocalClipboardToRemoteSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d2dd6fa5fc4d442d7cc22f036c293ebfaba841b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "105720240"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a><span data-ttu-id="f3b1a-106">IMsRdpClipboard:: CanSyncLocalClipboardToRemoteSession (método)</span><span class="sxs-lookup"><span data-stu-id="f3b1a-106">IMsRdpClipboard::CanSyncLocalClipboardToRemoteSession method</span></span>

<span data-ttu-id="f3b1a-107">Indica si el portapapeles local se puede sincronizar con la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-107">Indicates whether the local Clipboard can be synced to the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b1a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3b1a-108">Syntax</span></span>

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="f3b1a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3b1a-109">Parameters</span></span>

<span data-ttu-id="f3b1a-110">**True** si el portapapeles local se puede sincronizar con la sesión remota; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-110">**TRUE** if the local Clipboard can be synced to the remote session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3b1a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3b1a-111">Return value</span></span>

<span data-ttu-id="f3b1a-112">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="f3b1a-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b1a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3b1a-113">Requirements</span></span>

| <span data-ttu-id="f3b1a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3b1a-114">Requirement</span></span> | <span data-ttu-id="f3b1a-115">Value</span><span class="sxs-lookup"><span data-stu-id="f3b1a-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f3b1a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3b1a-116">Minimum supported client</span></span>| <span data-ttu-id="f3b1a-117">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="f3b1a-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="f3b1a-118">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f3b1a-118">Type library</span></span>            | <span data-ttu-id="f3b1a-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f3b1a-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f3b1a-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3b1a-120">DLL</span></span>                  | <span data-ttu-id="f3b1a-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f3b1a-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f3b1a-122">IID</span><span class="sxs-lookup"><span data-stu-id="f3b1a-122">IID</span></span>                      | <span data-ttu-id="f3b1a-123">IID \_ IMsRdpClipboard se define como 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="f3b1a-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="f3b1a-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3b1a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b1a-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="f3b1a-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>