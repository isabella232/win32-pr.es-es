---
title: Interfaz IMsRdpClipboard
description: Representa el controlador del portapapeles que se usa para sincronizar los portapapeles locales y remotos si está habilitada la sincronización manual del portapapeles.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClipboard
- Servicios de Escritorio remoto de la interfaz IMsRdpClipboard, descrito
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104151929"
---
# <a name="imsrdpclipboard-interface"></a><span data-ttu-id="d100c-105">Interfaz IMsRdpClipboard</span><span class="sxs-lookup"><span data-stu-id="d100c-105">IMsRdpClipboard interface</span></span>

<span data-ttu-id="d100c-106">Representa el controlador del portapapeles que se usa para sincronizar los portapapeles locales y remotos si está habilitada la sincronización manual del portapapeles (es decir, el valor de la propiedad [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) se establece en **true**).</span><span class="sxs-lookup"><span data-stu-id="d100c-106">Represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="members"></a><span data-ttu-id="d100c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d100c-107">Members</span></span>

<span data-ttu-id="d100c-108">La interfaz **IMsRdpClipboard** hereda de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="d100c-108">The **IMsRdpClipboard** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="d100c-109">**IMsRdpClipboard** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d100c-109">**IMsRdpClipboard** also has these types of members:</span></span>

- [<span data-ttu-id="d100c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d100c-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d100c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d100c-111">Methods</span></span>

<span data-ttu-id="d100c-112">La interfaz **IMsRdpClipboard** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d100c-112">The **IMsRdpClipboard** interface has these methods.</span></span>


| <span data-ttu-id="d100c-113">Método</span><span class="sxs-lookup"><span data-stu-id="d100c-113">Method</span></span>        | <span data-ttu-id="d100c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d100c-114">Description</span></span>      |
|:---------------|:----------------|
| [<span data-ttu-id="d100c-115">**CanSyncLocalClipboardToRemoteSession**</span><span class="sxs-lookup"><span data-stu-id="d100c-115">**CanSyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  <span data-ttu-id="d100c-116">Indica si el portapapeles local se puede sincronizar con la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="d100c-116">Indicates whether the local Clipboard can be synced to the remote session.</span></span>                   |
| [<span data-ttu-id="d100c-117">**CanSyncRemoteClipboardToLocalSession**</span><span class="sxs-lookup"><span data-stu-id="d100c-117">**CanSyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  <span data-ttu-id="d100c-118">Indica si el portapapeles remoto se puede sincronizar con la sesión local.</span><span class="sxs-lookup"><span data-stu-id="d100c-118">Indicates whether the remote Clipboard can be synced to the local session.</span></span>                   |
| [<span data-ttu-id="d100c-119">**SyncLocalClipboardToRemoteSession**</span><span class="sxs-lookup"><span data-stu-id="d100c-119">**SyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  <span data-ttu-id="d100c-120">Sincroniza el portapapeles local con la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="d100c-120">Syncs the local Clipboard to the remote session.</span></span>                   |
| [<span data-ttu-id="d100c-121">**SyncRemoteClipboardToLocalSession**</span><span class="sxs-lookup"><span data-stu-id="d100c-121">**SyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   <span data-ttu-id="d100c-122">Sincroniza el portapapeles remoto con la sesión local.</span><span class="sxs-lookup"><span data-stu-id="d100c-122">Syncs the remote Clipboard to the local session.</span></span>                      |

## <a name="requirements"></a><span data-ttu-id="d100c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d100c-123">Requirements</span></span>

| <span data-ttu-id="d100c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d100c-124">Requirement</span></span> | <span data-ttu-id="d100c-125">Value</span><span class="sxs-lookup"><span data-stu-id="d100c-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="d100c-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d100c-126">Minimum supported client</span></span>| <span data-ttu-id="d100c-127">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="d100c-127">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="d100c-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d100c-128">Type library</span></span>            | <span data-ttu-id="d100c-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d100c-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="d100c-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d100c-130">DLL</span></span>                  | <span data-ttu-id="d100c-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d100c-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="d100c-132">IID</span><span class="sxs-lookup"><span data-stu-id="d100c-132">IID</span></span>                      | <span data-ttu-id="d100c-133">IID \_ IMsRdpClipboard se define como 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="d100c-133">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>            |

## <a name="see-also"></a><span data-ttu-id="d100c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="d100c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d100c-135">**IMsRdpClientNonScriptable7:: Clipboard**</span><span class="sxs-lookup"><span data-stu-id="d100c-135">**IMsRdpClientNonScriptable7::Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
