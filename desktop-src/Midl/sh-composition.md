---
title: Palabra clave sh_composition
description: La \_ palabra clave \ SH Composition \ especifica que el objeto del sistema es un identificador de una superficie de composición.
keywords:
- palabra clave sh_composition MIDL
topic_type:
- apiref
api_name:
- sh_composition
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5a7e723c65ca6320dbec4a2f8a379cfed2f85f72
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104279724"
---
# <a name="sh_composition-keyword"></a><span data-ttu-id="61a1a-104">\_palabra clave de composición SH</span><span class="sxs-lookup"><span data-stu-id="61a1a-104">sh\_composition keyword</span></span>

<span data-ttu-id="61a1a-105">La palabra clave de **\_ composición SH** especifica que un `system_handle` contiene un identificador para una superficie de composición.</span><span class="sxs-lookup"><span data-stu-id="61a1a-105">The **sh\_composition** keyword specifies that a `system_handle` holds a handle to a composition surface.</span></span>

``` syntax
[system_handle(sh_composition)]

[system_handle(sh_composition, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="61a1a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61a1a-106">Parameters</span></span>

<span data-ttu-id="61a1a-107">Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="61a1a-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="61a1a-108">La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="61a1a-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="61a1a-109">El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="61a1a-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="61a1a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61a1a-110">Remarks</span></span>

<span data-ttu-id="61a1a-111">Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="61a1a-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="61a1a-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="61a1a-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetVisualSurface([out, system_handle(sh_composition)] HANDLE* visual);
}
```

## <a name="requirements"></a><span data-ttu-id="61a1a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61a1a-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="61a1a-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61a1a-114">Minimum supported client</span></span> | <span data-ttu-id="61a1a-115">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="61a1a-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="61a1a-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61a1a-116">Minimum supported server</span></span> | <span data-ttu-id="61a1a-117">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="61a1a-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="61a1a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="61a1a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a1a-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="61a1a-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="61a1a-120">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="61a1a-120">DirectComposition</span></span>](/windows/win32/api/_directcomp/)
</dt> <dt>

[<span data-ttu-id="61a1a-121">**DCompositionCreateSurfaceHandle** función)</span><span class="sxs-lookup"><span data-stu-id="61a1a-121">**DCompositionCreateSurfaceHandle** function</span></span>](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> </dl>
