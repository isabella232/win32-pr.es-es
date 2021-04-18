---
title: Método CanSyncRemoteClipboardToLocalSession de la interfaz IMsRdpClipboard
description: Indica si el portapapeles remoto se puede sincronizar con la sesión local.
ms.tgt_platform: multiple
keywords:
- Método CanSyncRemoteClipboardToLocalSession Servicios de Escritorio remoto
- Método CanSyncRemoteClipboardToLocalSession Servicios de Escritorio remoto, interfaz IMsRdpClipboard
- Interfaz IMsRdpClipboard Servicios de Escritorio remoto, método CanSyncRemoteClipboardToLocalSession
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "105720253"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a><span data-ttu-id="fa6a4-106">IMsRdpClipboard:: CanSyncRemoteClipboardToLocalSession (método)</span><span class="sxs-lookup"><span data-stu-id="fa6a4-106">IMsRdpClipboard::CanSyncRemoteClipboardToLocalSession method</span></span>

<span data-ttu-id="fa6a4-107">Indica si el portapapeles remoto se puede sincronizar con la sesión local.</span><span class="sxs-lookup"><span data-stu-id="fa6a4-107">Indicates whether the remote Clipboard can be synced to the local session.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa6a4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa6a4-108">Syntax</span></span>

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="fa6a4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa6a4-109">Parameters</span></span>

<span data-ttu-id="fa6a4-110">**True** si el portapapeles remoto se puede sincronizar con la sesión local; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="fa6a4-110">**TRUE** if the remote Clipboard can be synced to the local session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa6a4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa6a4-111">Return value</span></span>

<span data-ttu-id="fa6a4-112">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="fa6a4-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa6a4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa6a4-113">Requirements</span></span>

| <span data-ttu-id="fa6a4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa6a4-114">Requirement</span></span> | <span data-ttu-id="fa6a4-115">Value</span><span class="sxs-lookup"><span data-stu-id="fa6a4-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="fa6a4-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa6a4-116">Minimum supported client</span></span>| <span data-ttu-id="fa6a4-117">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="fa6a4-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="fa6a4-118">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fa6a4-118">Type library</span></span>            | <span data-ttu-id="fa6a4-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fa6a4-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="fa6a4-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa6a4-120">DLL</span></span>                  | <span data-ttu-id="fa6a4-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="fa6a4-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="fa6a4-122">IID</span><span class="sxs-lookup"><span data-stu-id="fa6a4-122">IID</span></span>                      | <span data-ttu-id="fa6a4-123">IID \_ IMsRdpClipboard se define como 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="fa6a4-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="fa6a4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa6a4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa6a4-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="fa6a4-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>