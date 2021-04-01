---
title: Estructura de ORPC_INIT_ARGS
description: La \_ estructura ORPC init \_ args contiene información que se usa para inicializar la depuración remota mediante la interfaz IOrpcDebugNotify.
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- Estructura de ORPC_INIT_ARGS COM
- LPORPC_INIT_ARGS puntero de estructura COM
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150081"
---
# <a name="orpc_init_args-structure"></a><span data-ttu-id="7a81b-105">ORPC \_ init \_ args (estructura)</span><span class="sxs-lookup"><span data-stu-id="7a81b-105">ORPC\_INIT\_ARGS structure</span></span>

<span data-ttu-id="7a81b-106">La estructura **ORPC \_ init \_ args** contiene información que se usa para inicializar la depuración remota mediante la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="7a81b-106">The **ORPC\_INIT\_ARGS** structure contains information used to initialize remote debugging using the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a81b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a81b-107">Syntax</span></span>


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a><span data-ttu-id="7a81b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a81b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a81b-109">**lpIntfOrpcDebug**</span><span class="sxs-lookup"><span data-stu-id="7a81b-109">**lpIntfOrpcDebug**</span></span>
</dt> <dd>

<span data-ttu-id="7a81b-110">Un puntero a la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) para su uso por los depuradores en proceso.</span><span class="sxs-lookup"><span data-stu-id="7a81b-110">A pointer to the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface for use by in-process debuggers.</span></span> <span data-ttu-id="7a81b-111">Si el depurador no está en proceso o es un sistema Macintosh, este campo debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="7a81b-111">If the debugger is not in-process or is a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7a81b-112">**pvPSN**</span><span class="sxs-lookup"><span data-stu-id="7a81b-112">**pvPSN**</span></span>
</dt> <dd>

<span data-ttu-id="7a81b-113">Puntero al número de serie del proceso de Macintosh del proceso del depurador.</span><span class="sxs-lookup"><span data-stu-id="7a81b-113">A pointer to the Macintosh process serial number of the debuggee's process.</span></span> <span data-ttu-id="7a81b-114">Si el código depurado no es un sistema Macintosh, este campo debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="7a81b-114">If the debuggee is not a Macintosh system, this field must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7a81b-115">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="7a81b-115">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="7a81b-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7a81b-116">Reserved.</span></span> <span data-ttu-id="7a81b-117">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="7a81b-117">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="7a81b-118">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="7a81b-118">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="7a81b-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7a81b-119">Reserved.</span></span> <span data-ttu-id="7a81b-120">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="7a81b-120">Must be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a81b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a81b-121">Requirements</span></span>



| <span data-ttu-id="7a81b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a81b-122">Requirement</span></span> | <span data-ttu-id="7a81b-123">Value</span><span class="sxs-lookup"><span data-stu-id="7a81b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="7a81b-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a81b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7a81b-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7a81b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="7a81b-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a81b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7a81b-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7a81b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7a81b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a81b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a81b-129"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="7a81b-129"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a81b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a81b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a81b-131">**ORPC \_ dbg \_ All**</span><span class="sxs-lookup"><span data-stu-id="7a81b-131">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="7a81b-132">**\_búfer ORPC dbg \_**</span><span class="sxs-lookup"><span data-stu-id="7a81b-132">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="7a81b-133">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="7a81b-133">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="7a81b-134">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="7a81b-134">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





