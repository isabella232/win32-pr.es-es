---
title: IOrpcDebugNotify ClientFillBuffer, método
description: Envía datos del depurador del cliente al depurador del servidor.
ms.assetid: d575cf34-34a2-4951-a87e-7835b2c5b7a0
keywords:
- Método ClientFillBuffer COM
- Método ClientFillBuffer COM, interfaz IOrpcDebugNotify
- Interfaz IOrpcDebugNotify COM, método ClientFillBuffer
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 633f4f0a8a3e135ca60468d24356a3f6e038d062
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803931"
---
# <a name="iorpcdebugnotifyclientfillbuffer-method"></a><span data-ttu-id="b0938-106">IOrpcDebugNotify:: ClientFillBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="b0938-106">IOrpcDebugNotify::ClientFillBuffer method</span></span>

<span data-ttu-id="b0938-107">Envía datos del depurador del cliente al depurador del servidor.</span><span class="sxs-lookup"><span data-stu-id="b0938-107">Sends data from the client debugger to the server debugger.</span></span>

> [!Note]  
> <span data-ttu-id="b0938-108">En el kit de desarrollo de software (SDK) de Microsoft Windows no se incluye una biblioteca de importación que contiene la función **ClientFillBuffer** .</span><span class="sxs-lookup"><span data-stu-id="b0938-108">An import library containing the **ClientFillBuffer** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b0938-109">Una aplicación puede usar las funciones [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar un puntero de función a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) desde oleaut.dll y proporcionar esta función a través de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="b0938-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b0938-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0938-110">Syntax</span></span>


```C++
void ClientFillBuffer(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="b0938-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0938-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0938-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="b0938-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="b0938-113">Un puntero a una estructura [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) que contiene información específica de la notificación que el sistema RPC de com pasa al depurador.</span><span class="sxs-lookup"><span data-stu-id="b0938-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0938-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0938-114">Return value</span></span>

<span data-ttu-id="b0938-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b0938-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0938-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0938-116">Requirements</span></span>



| <span data-ttu-id="b0938-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0938-117">Requirement</span></span> | <span data-ttu-id="b0938-118">Value</span><span class="sxs-lookup"><span data-stu-id="b0938-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b0938-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0938-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0938-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b0938-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="b0938-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0938-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0938-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b0938-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b0938-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0938-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0938-124"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="b0938-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="b0938-125">IDL</span><span class="sxs-lookup"><span data-stu-id="b0938-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0938-126"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="b0938-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0938-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0938-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0938-128">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="b0938-128">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="b0938-129">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="b0938-129">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

