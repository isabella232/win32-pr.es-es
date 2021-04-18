---
title: Palabra clave sh_event
description: La \_ palabra clave \ SH Event \ especifica que el objeto del sistema es un identificador de un evento.
keywords:
- palabra clave sh_event MIDL
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1a9b6dc7cc9dc4de4abd5dcc88a53588167db59d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "105721187"
---
# <a name="sh_event-keyword"></a><span data-ttu-id="ba7a4-104">SH \_ (palabra clave)</span><span class="sxs-lookup"><span data-stu-id="ba7a4-104">sh\_event keyword</span></span>

<span data-ttu-id="ba7a4-105">La palabra clave de **\_ evento SH** especifica que un `system_handle` contiene un identificador para un evento.</span><span class="sxs-lookup"><span data-stu-id="ba7a4-105">The **sh\_event** keyword specifies that a `system_handle` holds a handle to an event.</span></span>

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="ba7a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba7a4-106">Parameters</span></span>

<span data-ttu-id="ba7a4-107">Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="ba7a4-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="ba7a4-108">La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="ba7a4-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="ba7a4-109">El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="ba7a4-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba7a4-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba7a4-110">Remarks</span></span>

<span data-ttu-id="ba7a4-111">Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="ba7a4-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="ba7a4-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ba7a4-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
}
```

## <a name="requirements"></a><span data-ttu-id="ba7a4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba7a4-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="ba7a4-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba7a4-114">Minimum supported client</span></span> | <span data-ttu-id="ba7a4-115">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="ba7a4-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="ba7a4-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba7a4-116">Minimum supported server</span></span> | <span data-ttu-id="ba7a4-117">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="ba7a4-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ba7a4-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba7a4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba7a4-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="ba7a4-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="ba7a4-120">Objetos de evento</span><span class="sxs-lookup"><span data-stu-id="ba7a4-120">Event Objects</span></span>](../sync/event-objects.md)
</dt> <dt>

[<span data-ttu-id="ba7a4-121">Derechos de acceso y seguridad de objetos de sincronización</span><span class="sxs-lookup"><span data-stu-id="ba7a4-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="ba7a4-122">**CreateEvent** (función)</span><span class="sxs-lookup"><span data-stu-id="ba7a4-122">**CreateEvent** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="ba7a4-123">**CreateEventEx** función)</span><span class="sxs-lookup"><span data-stu-id="ba7a4-123">**CreateEventEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
