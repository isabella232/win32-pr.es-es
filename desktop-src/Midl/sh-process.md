---
title: Palabra clave sh_process
description: La \_ palabra clave \ SH Process \ especifica que el objeto del sistema es un identificador de un proceso.
keywords:
- palabra clave sh_process MIDL
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3652c6889c687173bbf7b397cddff4659c0329f1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "105721193"
---
# <a name="sh_process-keyword"></a><span data-ttu-id="e098f-104">SH \_ (palabra clave de proceso)</span><span class="sxs-lookup"><span data-stu-id="e098f-104">sh\_process keyword</span></span>

<span data-ttu-id="e098f-105">La palabra clave de **\_ proceso SH** especifica que un `system_handle` contiene un identificador de un proceso.</span><span class="sxs-lookup"><span data-stu-id="e098f-105">The **sh\_process** keyword specifies that a `system_handle` holds a handle to a process.</span></span>

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="e098f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e098f-106">Parameters</span></span>

<span data-ttu-id="e098f-107">Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="e098f-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="e098f-108">La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="e098f-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="e098f-109">El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="e098f-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="e098f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e098f-110">Remarks</span></span>

<span data-ttu-id="e098f-111">Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="e098f-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="e098f-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e098f-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="e098f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e098f-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="e098f-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e098f-114">Minimum supported client</span></span> | <span data-ttu-id="e098f-115">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="e098f-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="e098f-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e098f-116">Minimum supported server</span></span> | <span data-ttu-id="e098f-117">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="e098f-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e098f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e098f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e098f-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="e098f-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="e098f-120">Acerca de los procesos y los subprocesos</span><span class="sxs-lookup"><span data-stu-id="e098f-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="e098f-121">Seguridad del proceso y derechos de acceso</span><span class="sxs-lookup"><span data-stu-id="e098f-121">Process Security and Access Rights</span></span>](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="e098f-122">**CreateProcess** (función)</span><span class="sxs-lookup"><span data-stu-id="e098f-122">**CreateProcess** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[<span data-ttu-id="e098f-123">**OpenProcess** (función)</span><span class="sxs-lookup"><span data-stu-id="e098f-123">**OpenProcess** function</span></span>](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>