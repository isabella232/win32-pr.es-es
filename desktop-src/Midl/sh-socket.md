---
title: Palabra clave sh_socket
description: La \_ palabra clave \ SH socket \ especifica que el objeto del sistema es un identificador de un socket.
keywords:
- palabra clave sh_socket MIDL
topic_type:
- apiref
api_name:
- sh_socket keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5f5d2506f66f89cd47ecf3f011c8071b79e64177
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "105721190"
---
# <a name="sh_socket-keyword"></a><span data-ttu-id="d60b2-104">SH \_ socket (palabra clave)</span><span class="sxs-lookup"><span data-stu-id="d60b2-104">sh\_socket keyword</span></span>

<span data-ttu-id="d60b2-105">La palabra clave de **SH \_ socket** especifica que un `system_handle` contiene un identificador de un socket.</span><span class="sxs-lookup"><span data-stu-id="d60b2-105">The **sh\_socket** keyword specifies that a `system_handle` holds a handle to a socket.</span></span>

``` syntax
[system_handle(sh_socket)]

[system_handle(sh_socket, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="d60b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d60b2-106">Parameters</span></span>

<span data-ttu-id="d60b2-107">Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="d60b2-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="d60b2-108">La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="d60b2-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="d60b2-109">El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="d60b2-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="d60b2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d60b2-110">Remarks</span></span>

<span data-ttu-id="d60b2-111">Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="d60b2-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="d60b2-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d60b2-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT ListenToSocket([in, system_handle(sh_socket)] HANDLE socket);
}
```

## <a name="requirements"></a><span data-ttu-id="d60b2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d60b2-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="d60b2-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d60b2-114">Minimum supported client</span></span> | <span data-ttu-id="d60b2-115">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="d60b2-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="d60b2-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d60b2-116">Minimum supported server</span></span> | <span data-ttu-id="d60b2-117">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="d60b2-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d60b2-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d60b2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d60b2-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="d60b2-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="d60b2-120">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="d60b2-120">Windows Sockets 2</span></span>](../winsock/windows-sockets-start-page-2.md)
</dt> </dl>
