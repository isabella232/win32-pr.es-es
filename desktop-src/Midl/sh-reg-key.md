---
title: Palabra clave sh_reg_key
description: La palabra clave \ SH \_ reg \_ key \ especifica que el objeto del sistema es un identificador de una clave del registro.
keywords:
- palabra clave sh_reg_key MIDL
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: cec526bed766534f82d5a1bc24c55050dea814ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "105721192"
---
# <a name="sh_reg_key-keyword"></a><span data-ttu-id="2013b-104">palabra clave de SH \_ reg \_</span><span class="sxs-lookup"><span data-stu-id="2013b-104">sh\_reg\_key keyword</span></span>

<span data-ttu-id="2013b-105">La palabra clave de **SH \_ reg \_ key** especifica que un `system_handle` contiene un identificador para una clave del registro.</span><span class="sxs-lookup"><span data-stu-id="2013b-105">The **sh\_reg\_key** keyword specifies that a `system_handle` holds a handle to a registry key.</span></span>

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="2013b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2013b-106">Parameters</span></span>

<span data-ttu-id="2013b-107">Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).</span><span class="sxs-lookup"><span data-stu-id="2013b-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="2013b-108">La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* .</span><span class="sxs-lookup"><span data-stu-id="2013b-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="2013b-109">El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="2013b-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="2013b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2013b-110">Remarks</span></span>

<span data-ttu-id="2013b-111">Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.</span><span class="sxs-lookup"><span data-stu-id="2013b-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="2013b-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2013b-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
}
```

## <a name="requirements"></a><span data-ttu-id="2013b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2013b-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="2013b-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2013b-114">Minimum supported client</span></span> | <span data-ttu-id="2013b-115">Actualización de aniversario de Windows 10 (versión 1607, compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="2013b-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="2013b-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2013b-116">Minimum supported server</span></span> | <span data-ttu-id="2013b-117">Windows Server 2016 (compilación 14393)</span><span class="sxs-lookup"><span data-stu-id="2013b-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="2013b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2013b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2013b-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="2013b-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="2013b-120">Registro</span><span class="sxs-lookup"><span data-stu-id="2013b-120">Registry</span></span>](../sysinfo/registry.md)
</dt> <dt>

[<span data-ttu-id="2013b-121">Seguridad y derechos de acceso de la clave del registro</span><span class="sxs-lookup"><span data-stu-id="2013b-121">Registry Key Security and Access Rights</span></span>](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="2013b-122">**RegOpenKeyEx** (función)</span><span class="sxs-lookup"><span data-stu-id="2013b-122">**RegOpenKeyEx** function</span></span>](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
