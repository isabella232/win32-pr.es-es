---
title: IOrpcDebugNotify ClientNotify, método
description: Informa al cliente de una solicitud de depurador saliente al servidor.
ms.assetid: a41e3eaa-6d1f-46bf-9103-f83e45b2cd90
keywords:
- Método ClientNotify COM
- Método ClientNotify COM, interfaz IOrpcDebugNotify
- Interfaz IOrpcDebugNotify COM, método ClientNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e788a51e278df09715aaf9d4993ac5724ed65b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493084"
---
# <a name="iorpcdebugnotifyclientnotify-method"></a><span data-ttu-id="8fe94-106">IOrpcDebugNotify:: ClientNotify (método)</span><span class="sxs-lookup"><span data-stu-id="8fe94-106">IOrpcDebugNotify::ClientNotify method</span></span>

<span data-ttu-id="8fe94-107">Informa al cliente de una solicitud de depurador saliente al servidor.</span><span class="sxs-lookup"><span data-stu-id="8fe94-107">Informs the client of an outgoing debugger request to the server.</span></span>

> [!Note]  
> <span data-ttu-id="8fe94-108">En el kit de desarrollo de software (SDK) de Microsoft Windows no se incluye una biblioteca de importación que contiene la función **ClientNotify** .</span><span class="sxs-lookup"><span data-stu-id="8fe94-108">An import library containing the **ClientNotify** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8fe94-109">Una aplicación puede usar las funciones [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar un puntero de función a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) desde oleaut.dll y proporcionar esta función a través de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="8fe94-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8fe94-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fe94-110">Syntax</span></span>


```C++
void ClientNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="8fe94-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fe94-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe94-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="8fe94-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="8fe94-113">Un puntero a una estructura [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) que contiene información específica de la notificación que el sistema RPC de com pasa al depurador.</span><span class="sxs-lookup"><span data-stu-id="8fe94-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe94-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fe94-114">Return value</span></span>

<span data-ttu-id="8fe94-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8fe94-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe94-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fe94-116">Requirements</span></span>



| <span data-ttu-id="8fe94-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fe94-117">Requirement</span></span> | <span data-ttu-id="8fe94-118">Value</span><span class="sxs-lookup"><span data-stu-id="8fe94-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="8fe94-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fe94-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe94-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8fe94-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="8fe94-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8fe94-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe94-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8fe94-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8fe94-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fe94-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fe94-124"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="8fe94-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="8fe94-125">IDL</span><span class="sxs-lookup"><span data-stu-id="8fe94-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8fe94-126"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="8fe94-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe94-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fe94-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe94-128">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="8fe94-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="8fe94-129">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="8fe94-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="8fe94-130">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="8fe94-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

