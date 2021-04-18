---
title: DllDebugObjectRPCHook función)
description: Exportado por DLL COM para habilitar la depuración remota.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- DllDebugObjectRPCHook función COM
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714641"
---
# <a name="dlldebugobjectrpchook-function"></a><span data-ttu-id="35895-104">DllDebugObjectRPCHook función)</span><span class="sxs-lookup"><span data-stu-id="35895-104">DllDebugObjectRPCHook function</span></span>

<span data-ttu-id="35895-105">Exportado por DLL COM para habilitar la depuración remota.</span><span class="sxs-lookup"><span data-stu-id="35895-105">Exported by COM DLLs to enable remote debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="35895-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35895-106">Syntax</span></span>


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a><span data-ttu-id="35895-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35895-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35895-108">*fTrace*</span><span class="sxs-lookup"><span data-stu-id="35895-108">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="35895-109">Si es **true**, se habilita la depuración remota.</span><span class="sxs-lookup"><span data-stu-id="35895-109">If **TRUE**, remote debugging is enabled.</span></span> <span data-ttu-id="35895-110">Si es **false**, la depuración remota no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="35895-110">If **FALSE**, remote debugging is not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="35895-111">*lpOrpcInitArgs*</span><span class="sxs-lookup"><span data-stu-id="35895-111">*lpOrpcInitArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="35895-112">Puntero a una estructura [**ORPC \_ init \_ args**](orpc-init-args.md) .</span><span class="sxs-lookup"><span data-stu-id="35895-112">A pointer to an [**ORPC\_INIT\_ARGS**](orpc-init-args.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35895-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35895-113">Return value</span></span>

<span data-ttu-id="35895-114">**True** si es correcto, **false** en caso contrario</span><span class="sxs-lookup"><span data-stu-id="35895-114">**TRUE** if successful, **FALSE** otherwise</span></span>

## <a name="requirements"></a><span data-ttu-id="35895-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35895-115">Requirements</span></span>



| <span data-ttu-id="35895-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="35895-116">Requirement</span></span> | <span data-ttu-id="35895-117">Value</span><span class="sxs-lookup"><span data-stu-id="35895-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35895-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35895-118">Minimum supported client</span></span><br/> | <span data-ttu-id="35895-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="35895-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="35895-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35895-120">Minimum supported server</span></span><br/> | <span data-ttu-id="35895-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="35895-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="35895-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35895-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="35895-123"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="35895-123"><dt>N/A</dt></span></span> </dl>       |
| <span data-ttu-id="35895-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35895-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="35895-125"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35895-125"><dt>Ole32.lib</dt></span></span> </dl> |
| <span data-ttu-id="35895-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35895-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35895-127"><dt>Ole32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35895-127"><dt>Ole32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35895-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="35895-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35895-129">**ORPC \_ dbg \_ All**</span><span class="sxs-lookup"><span data-stu-id="35895-129">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="35895-130">**\_búfer ORPC dbg \_**</span><span class="sxs-lookup"><span data-stu-id="35895-130">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="35895-131">**ORPC \_ init \_ args**</span><span class="sxs-lookup"><span data-stu-id="35895-131">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="35895-132">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="35895-132">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





