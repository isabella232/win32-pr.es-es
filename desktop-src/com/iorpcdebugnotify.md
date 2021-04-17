---
title: Interfaz IOrpcDebugNotify
description: Proporciona la funcionalidad de depuración remota.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- Interfaz IOrpcDebugNotify COM
- Interfaz IOrpcDebugNotify COM, descripción
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535440"
---
# <a name="iorpcdebugnotify-interface"></a><span data-ttu-id="a9b4e-105">Interfaz IOrpcDebugNotify</span><span class="sxs-lookup"><span data-stu-id="a9b4e-105">IOrpcDebugNotify interface</span></span>

<span data-ttu-id="a9b4e-106">Proporciona la funcionalidad de depuración remota.</span><span class="sxs-lookup"><span data-stu-id="a9b4e-106">Provides remote debugging functionality.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="a9b4e-107">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="a9b4e-107">When to implement</span></span>

<span data-ttu-id="a9b4e-108">Implemente esta interfaz para habilitar la depuración remota a través de RPC.</span><span class="sxs-lookup"><span data-stu-id="a9b4e-108">Implement this interface to enable remote debugging over RPC.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a9b4e-109">Cuándo se usa</span><span class="sxs-lookup"><span data-stu-id="a9b4e-109">When to use</span></span>

<span data-ttu-id="a9b4e-110">Esta interfaz se debe usar para la depuración remota en proceso cuando las excepciones de software no deben usarse para las notificaciones del depurador COM.</span><span class="sxs-lookup"><span data-stu-id="a9b4e-110">This interface should be used for in-process remote debugging when software exceptions should not be used for the COM debugger notifications.</span></span> <span data-ttu-id="a9b4e-111">Permite a los depuradores en proceso recibir notificaciones directas mediante el uso de estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a9b4e-111">It enables in-process debuggers to be notified by direct calls using these methods.</span></span>

## <a name="members"></a><span data-ttu-id="a9b4e-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="a9b4e-112">Members</span></span>

<span data-ttu-id="a9b4e-113">La interfaz **IOrpcDebugNotify** hereda de la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a9b4e-113">The **IOrpcDebugNotify** interface inherits from the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a9b4e-114">**IOrpcDebugNotify** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a9b4e-114">**IOrpcDebugNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="a9b4e-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9b4e-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a9b4e-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9b4e-116">Methods</span></span>

<span data-ttu-id="a9b4e-117">La interfaz **IOrpcDebugNotify** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a9b4e-117">The **IOrpcDebugNotify** interface has these methods.</span></span>



| <span data-ttu-id="a9b4e-118">Método</span><span class="sxs-lookup"><span data-stu-id="a9b4e-118">Method</span></span>                                                              | <span data-ttu-id="a9b4e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9b4e-119">Description</span></span>                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="a9b4e-120">**ClientFillBuffer**</span><span class="sxs-lookup"><span data-stu-id="a9b4e-120">**ClientFillBuffer**</span></span>](iorpcdebugnotify-clientfillbuffer.md)       | <span data-ttu-id="a9b4e-121">Envía datos del depurador del cliente al depurador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a9b4e-121">Sends data from the client debugger to the server debugger.</span></span><br/>         |
| [<span data-ttu-id="a9b4e-122">**ClientGetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="a9b4e-122">**ClientGetBufferSize**</span></span>](iorpcdebugnotify-clientgetbuffersize.md) | <span data-ttu-id="a9b4e-123">Recupera el tamaño del búfer de RPC desde el depurador del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="a9b4e-123">Retrieves the RPC buffer size from the client-side debugger.</span></span><br/>        |
| [<span data-ttu-id="a9b4e-124">**ClientNotify**</span><span class="sxs-lookup"><span data-stu-id="a9b4e-124">**ClientNotify**</span></span>](iorpcdebugnotify-clientnotify.md)               | <span data-ttu-id="a9b4e-125">Informa al cliente de una solicitud de depurador saliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="a9b4e-125">Informs the client of an outgoing debugger request to the server.</span></span><br/>   |
| [<span data-ttu-id="a9b4e-126">**ServerFillBuffer**</span><span class="sxs-lookup"><span data-stu-id="a9b4e-126">**ServerFillBuffer**</span></span>](iorpcdebugnotify-serverfillbuffer.md)       | <span data-ttu-id="a9b4e-127">Envía datos del depurador del servidor al depurador del cliente.</span><span class="sxs-lookup"><span data-stu-id="a9b4e-127">Sends data from the server debugger to the client debugger.</span></span><br/>         |
| [<span data-ttu-id="a9b4e-128">**ServerGetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="a9b4e-128">**ServerGetBufferSize**</span></span>](iorpcdebugnotify-servergetbuffersize.md) | <span data-ttu-id="a9b4e-129">Recupera el tamaño del búfer de RPC desde el depurador del servidor.</span><span class="sxs-lookup"><span data-stu-id="a9b4e-129">Retrieves the RPC buffer size from the server-side debugger.</span></span><br/>        |
| [<span data-ttu-id="a9b4e-130">**ServerNotify**</span><span class="sxs-lookup"><span data-stu-id="a9b4e-130">**ServerNotify**</span></span>](iorpcdebugnotify-servernotify.md)               | <span data-ttu-id="a9b4e-131">Informa al servidor de una solicitud de depurador entrante del cliente.</span><span class="sxs-lookup"><span data-stu-id="a9b4e-131">Informs the server of an incoming debugger request from the client.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a9b4e-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9b4e-132">Remarks</span></span>

<span data-ttu-id="a9b4e-133">En el kit de desarrollo de software (SDK) de Microsoft Windows no se incluye una biblioteca de importación que contiene la interfaz **IOrpcDebugNotify** .</span><span class="sxs-lookup"><span data-stu-id="a9b4e-133">An import library containing the **IOrpcDebugNotify** interface is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a9b4e-134">Una aplicación puede usar las funciones [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar un puntero de función a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) desde oleaut.dll y proporcionar estos métodos a través de la interfaz **IOrpcDebugNotify** .</span><span class="sxs-lookup"><span data-stu-id="a9b4e-134">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide these methods via the **IOrpcDebugNotify** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9b4e-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9b4e-135">Requirements</span></span>



| <span data-ttu-id="a9b4e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9b4e-136">Requirement</span></span> | <span data-ttu-id="a9b4e-137">Value</span><span class="sxs-lookup"><span data-stu-id="a9b4e-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a9b4e-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9b4e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a9b4e-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a9b4e-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="a9b4e-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9b4e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a9b4e-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a9b4e-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a9b4e-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9b4e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9b4e-143"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="a9b4e-143"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="a9b4e-144">IDL</span><span class="sxs-lookup"><span data-stu-id="a9b4e-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9b4e-145"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="a9b4e-145"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9b4e-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9b4e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9b4e-147">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="a9b4e-147">**IUnknown**</span></span>](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[<span data-ttu-id="a9b4e-148">**ORPC \_ dbg \_ All**</span><span class="sxs-lookup"><span data-stu-id="a9b4e-148">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="a9b4e-149">**\_búfer ORPC dbg \_**</span><span class="sxs-lookup"><span data-stu-id="a9b4e-149">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="a9b4e-150">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="a9b4e-150">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="a9b4e-151">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="a9b4e-151">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> </dl>

 

