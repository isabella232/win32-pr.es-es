---
title: IMsTscAxEvents OnEnterFullScreenMode, método
description: Se llama cuando el cliente entra en el modo de pantalla completa. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de teclas de método abreviado del modo de pantalla completa (CTRL + ALT + inter).
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- Método OnEnterFullScreenMode Servicios de Escritorio remoto
- Método OnEnterFullScreenMode Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnEnterFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnEnterFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226054fc7b1371bb088deb70ec9e87ea5a340b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996592"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a><span data-ttu-id="85e72-107">IMsTscAxEvents:: OnEnterFullScreenMode (método)</span><span class="sxs-lookup"><span data-stu-id="85e72-107">IMsTscAxEvents::OnEnterFullScreenMode method</span></span>

<span data-ttu-id="85e72-108">Se llama cuando el cliente entra en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="85e72-108">Called when the client enters full-screen mode.</span></span> <span data-ttu-id="85e72-109">Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de [teclas de método abreviado](terminal-services-shortcut-keys.md) del modo de pantalla completa (Ctrl + Alt + inter).</span><span class="sxs-lookup"><span data-stu-id="85e72-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="85e72-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85e72-110">Syntax</span></span>


```C++
void OnEnterFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="85e72-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85e72-111">Parameters</span></span>

<span data-ttu-id="85e72-112">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="85e72-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85e72-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85e72-113">Return value</span></span>

<span data-ttu-id="85e72-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="85e72-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85e72-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85e72-115">Remarks</span></span>

<span data-ttu-id="85e72-116">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="85e72-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85e72-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85e72-117">Requirements</span></span>



| <span data-ttu-id="85e72-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="85e72-118">Requirement</span></span> | <span data-ttu-id="85e72-119">Value</span><span class="sxs-lookup"><span data-stu-id="85e72-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85e72-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85e72-120">Minimum supported client</span></span><br/> | <span data-ttu-id="85e72-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85e72-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="85e72-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85e72-122">Minimum supported server</span></span><br/> | <span data-ttu-id="85e72-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85e72-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="85e72-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="85e72-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="85e72-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85e72-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="85e72-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85e72-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85e72-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85e72-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="85e72-128">IID</span><span class="sxs-lookup"><span data-stu-id="85e72-128">IID</span></span><br/>                      | <span data-ttu-id="85e72-129">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="85e72-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="85e72-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="85e72-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e72-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="85e72-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





