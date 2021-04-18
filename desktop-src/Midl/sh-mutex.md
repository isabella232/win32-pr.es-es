---
title: Palabra clave sh_mutex
description: La \_ palabra clave \ SH mutex \ especifica que el objeto del sistema es un identificador de una exclusión mutua.
keywords:
- palabra clave sh_mutex MIDL
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721387"
---
# <a name="sh_mutex-keyword"></a><span data-ttu-id="e0875-104">SH \_ (palabra clave mutex)</span><span class="sxs-lookup"><span data-stu-id="e0875-104">sh\_mutex keyword</span></span>

<span data-ttu-id="e0875-105">La palabra clave de **\_ exclusión mutua SH** especifica que un `system_handle` contiene un identificador para una exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="e0875-105">The **sh\_mutex** keyword specifies that a `system_handle` holds a handle to a mutex.</span></span>

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="e0875-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0875-106">Parameters</span></span>

<span data-ttu-id="e0875-107">Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="e0875-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="e0875-108">La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="e0875-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="e0875-109">El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="e0875-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0875-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0875-110">Remarks</span></span>

<span data-ttu-id="e0875-111">Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="e0875-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="e0875-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e0875-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
}
```

## <a name="requirements"></a><span data-ttu-id="e0875-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0875-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="e0875-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0875-114">Minimum supported client</span></span> | <span data-ttu-id="e0875-115">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="e0875-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="e0875-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0875-116">Minimum supported server</span></span> | <span data-ttu-id="e0875-117">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="e0875-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e0875-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0875-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0875-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="e0875-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="e0875-120">Objetos mutex</span><span class="sxs-lookup"><span data-stu-id="e0875-120">Mutex Objects</span></span>](../sync/mutex-objects.md)
</dt> <dt>

[<span data-ttu-id="e0875-121">Derechos de acceso y seguridad de objetos de sincronización</span><span class="sxs-lookup"><span data-stu-id="e0875-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="e0875-122">**CreateMutex** (función)</span><span class="sxs-lookup"><span data-stu-id="e0875-122">**CreateMutex** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[<span data-ttu-id="e0875-123">**CreateMutexEx** función)</span><span class="sxs-lookup"><span data-stu-id="e0875-123">**CreateMutexEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>