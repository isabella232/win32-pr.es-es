---
title: Palabra clave sh_pipe
description: La \_ palabra clave \ SH Pipe \ especifica que el objeto del sistema es un identificador de una canalización.
keywords:
- palabra clave sh_pipe MIDL
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 9f9deab2bf5a751d3b2d5956d4d33a1d5b347e18
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "105721184"
---
# <a name="sh_pipe-keyword"></a><span data-ttu-id="f55c1-104">SH \_ Pipe (palabra clave)</span><span class="sxs-lookup"><span data-stu-id="f55c1-104">sh\_pipe keyword</span></span>

<span data-ttu-id="f55c1-105">La palabra clave **SH \_ Pipe** especifica que un `system_handle` contiene un identificador a una canalización.</span><span class="sxs-lookup"><span data-stu-id="f55c1-105">The **sh\_pipe** keyword specifies that a `system_handle` holds a handle to a pipe.</span></span>

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="f55c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f55c1-106">Parameters</span></span>

<span data-ttu-id="f55c1-107">Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="f55c1-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="f55c1-108">La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="f55c1-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="f55c1-109">El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="f55c1-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="f55c1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f55c1-110">Remarks</span></span>

<span data-ttu-id="f55c1-111">Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="f55c1-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="f55c1-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f55c1-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
}
```

## <a name="requirements"></a><span data-ttu-id="f55c1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f55c1-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="f55c1-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f55c1-114">Minimum supported client</span></span> | <span data-ttu-id="f55c1-115">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="f55c1-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="f55c1-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f55c1-116">Minimum supported server</span></span> | <span data-ttu-id="f55c1-117">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="f55c1-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="f55c1-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f55c1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f55c1-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="f55c1-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="f55c1-120">Acerca de las canalizaciones</span><span class="sxs-lookup"><span data-stu-id="f55c1-120">About Pipes</span></span>](../ipc/about-pipes.md)
</dt> <dt>

[<span data-ttu-id="f55c1-121">Derechos de acceso y seguridad de archivos</span><span class="sxs-lookup"><span data-stu-id="f55c1-121">File Security and Access Rights</span></span>](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="f55c1-122">**CreatePipe** función)</span><span class="sxs-lookup"><span data-stu-id="f55c1-122">**CreatePipe** function</span></span>](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[<span data-ttu-id="f55c1-123">**CreateNamedPipe** función)</span><span class="sxs-lookup"><span data-stu-id="f55c1-123">**CreateNamedPipe** function</span></span>](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
