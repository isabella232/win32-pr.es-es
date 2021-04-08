---
title: Palabra clave sh_job
description: La \_ palabra clave \ SH Job \ especifica que el objeto del sistema es un identificador de un trabajo.
keywords:
- palabra clave sh_job MIDL
topic_type:
- apiref
api_name:
- sh_job
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: db24f9dc84f2bb56f57327090485b406ad1a437f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104003275"
---
# <a name="sh_job-keyword"></a><span data-ttu-id="fe010-104">\_palabra clave de trabajo SH</span><span class="sxs-lookup"><span data-stu-id="fe010-104">sh\_job keyword</span></span>

<span data-ttu-id="fe010-105">La palabra clave de **\_ trabajo SH** especifica que un `system_handle` contiene un identificador de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="fe010-105">The **sh\_job** keyword specifies that a `system_handle` holds a handle to a job.</span></span>

``` syntax
[system_handle(sh_job)]

[system_handle(sh_job, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="fe010-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe010-106">Parameters</span></span>

<span data-ttu-id="fe010-107">Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="fe010-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="fe010-108">La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="fe010-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="fe010-109">El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="fe010-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe010-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe010-110">Remarks</span></span>

<span data-ttu-id="fe010-111">Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="fe010-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="fe010-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fe010-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetJob([in, system_handle(sh_job)] HANDLE job);

    HRESULT GetJobForAccounting([out, system_handle(sh_job, JOB_OBJECT_QUERY)] HANDLE* pJob);
}
```

## <a name="requirements"></a><span data-ttu-id="fe010-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe010-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="fe010-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe010-114">Minimum supported client</span></span> | <span data-ttu-id="fe010-115">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="fe010-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="fe010-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe010-116">Minimum supported server</span></span> | <span data-ttu-id="fe010-117">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="fe010-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="fe010-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe010-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe010-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="fe010-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="fe010-120">Objetos de trabajo</span><span class="sxs-lookup"><span data-stu-id="fe010-120">Job Objects</span></span>](../procthread/job-objects.md)
</dt> <dt>

[<span data-ttu-id="fe010-121">Derechos de acceso y seguridad de objetos de trabajo</span><span class="sxs-lookup"><span data-stu-id="fe010-121">Job Object Security and Access Rights</span></span>](../procthread/job-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="fe010-122">**CreateJobObject** función)</span><span class="sxs-lookup"><span data-stu-id="fe010-122">**CreateJobObject** function</span></span>](/windows/win32/api/winbase/nf-winbase-createjobobjecta)
</dt> </dl>
