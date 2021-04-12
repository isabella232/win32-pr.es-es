---
title: Palabra clave sh_file
description: La \_ palabra clave \ SH File \ especifica que el objeto del sistema es un identificador de un archivo.
keywords:
- palabra clave sh_file MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: f7d2ae0ef4a8166f90700267fa8459525ad4be2f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104361792"
---
# <a name="sh_file-keyword"></a><span data-ttu-id="cfdb1-104">SH \_ archivo (palabra clave)</span><span class="sxs-lookup"><span data-stu-id="cfdb1-104">sh\_file keyword</span></span>

<span data-ttu-id="cfdb1-105">La palabra clave **SH \_ File** especifica que un `system_handle` contiene un identificador de un archivo.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-105">The **sh\_file** keyword specifies that a `system_handle` holds a handle to a file.</span></span>

``` syntax
[system_handle(sh_file)]

[system_handle(sh_file, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="cfdb1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfdb1-106">Parameters</span></span>

<span data-ttu-id="cfdb1-107">Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="cfdb1-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="cfdb1-108">La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="cfdb1-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="cfdb1-109">El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="cfdb1-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfdb1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfdb1-110">Remarks</span></span>

<span data-ttu-id="cfdb1-111">Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="cfdb1-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="cfdb1-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cfdb1-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WriteThisFile([in, system_handle(sh_file)] HANDLE file);

    HRESULT GetFileToRead([out, system_handle(sh_file, READ_CONTROL | SYNCHRONIZE | FILE_READ_DATA | FILE_READ_keywordS | FILE_READ_EA)] HANDLE* pReadThisFile);
}
```

## <a name="requirements"></a><span data-ttu-id="cfdb1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfdb1-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="cfdb1-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfdb1-114">Minimum supported client</span></span> | <span data-ttu-id="cfdb1-115">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="cfdb1-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="cfdb1-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfdb1-116">Minimum supported server</span></span> | <span data-ttu-id="cfdb1-117">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="cfdb1-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="cfdb1-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfdb1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfdb1-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="cfdb1-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="cfdb1-120">Derechos de acceso y seguridad de archivos</span><span class="sxs-lookup"><span data-stu-id="cfdb1-120">File Security and Access Rights</span></span>](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="cfdb1-121">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="cfdb1-121">DirectComposition</span></span>](/windows/win32/api/_directcomp/)
</dt> <dt>

[<span data-ttu-id="cfdb1-122">**DCompositionCreateSurfaceHandle** función)</span><span class="sxs-lookup"><span data-stu-id="cfdb1-122">**DCompositionCreateSurfaceHandle** function</span></span>](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> <dt>
