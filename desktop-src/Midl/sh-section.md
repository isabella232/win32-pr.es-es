---
title: Palabra clave sh_section
description: La \_ palabra clave \ SH Section \ especifica que el objeto del sistema es un identificador de una sección.
keywords:
- palabra clave sh_section MIDL
topic_type:
- apiref
api_name:
- sh_section keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 056112deb790e727206a5ac1a1a2a5043a68f5e1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "105721191"
---
# <a name="sh_section-keyword"></a><span data-ttu-id="7665b-104">\_palabra clave de la sección SH</span><span class="sxs-lookup"><span data-stu-id="7665b-104">sh\_section keyword</span></span>

<span data-ttu-id="7665b-105">La palabra clave de la **\_ sección SH** especifica que un `system_handle` contiene un identificador de una sección.</span><span class="sxs-lookup"><span data-stu-id="7665b-105">The **sh\_section** keyword specifies that a `system_handle` holds a handle to a section.</span></span>

``` syntax
[system_handle(sh_section)]

[system_handle(sh_section, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="7665b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7665b-106">Parameters</span></span>

<span data-ttu-id="7665b-107">Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="7665b-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="7665b-108">La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="7665b-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="7665b-109">El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="7665b-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="7665b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7665b-110">Remarks</span></span>

<span data-ttu-id="7665b-111">Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="7665b-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="7665b-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7665b-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GiveSection([in, system_handle(sh_section)] HANDLE section);

    HRESULT GetSectionToWatch([out, system_handle(sh_section, SECTION_MAP_READ)] HANDLE* pSection);
}
```

## <a name="requirements"></a><span data-ttu-id="7665b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7665b-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="7665b-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7665b-114">Minimum supported client</span></span> | <span data-ttu-id="7665b-115">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="7665b-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="7665b-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7665b-116">Minimum supported server</span></span> | <span data-ttu-id="7665b-117">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="7665b-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="7665b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="7665b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7665b-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="7665b-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="7665b-120">Objetos y vistas de la sección</span><span class="sxs-lookup"><span data-stu-id="7665b-120">Section Objects and Views</span></span>](/windows-hardware/drivers/kernel/section-objects-and-views)
</dt> <dt>

[<span data-ttu-id="7665b-121">Función **ZwCreateSection** (incluidas las especificaciones de acceso)</span><span class="sxs-lookup"><span data-stu-id="7665b-121">**ZwCreateSection** function (including access specifications)</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-zwcreatesection)
</dt> </dl>
