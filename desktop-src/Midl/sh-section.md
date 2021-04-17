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
# <a name="sh_section-keyword"></a>\_palabra clave de la sección SH

La palabra clave de la **\_ sección SH** especifica que un `system_handle` contiene un identificador de una sección.

``` syntax
[system_handle(sh_section)]

[system_handle(sh_section, access-rights)]
```

## <a name="parameters"></a>Parámetros

Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).

La documentación [**system_handle**](system-handle.md) contiene también detalles sobre el uso opcional del parámetro *Access-Rights* . El comportamiento predeterminado es `DUPLICATE_SAME_ACCESS` por especificaciones de la [función **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

## <a name="remarks"></a>Observaciones

Para usar esta palabra clave con el `system_handle` atributo, la `-target` marca debe establecerse en `NT100` (o superior) al ejecutarse midl.exe.

## <a name="examples"></a>Ejemplos

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GiveSection([in, system_handle(sh_section)] HANDLE section);

    HRESULT GetSectionToWatch([out, system_handle(sh_section, SECTION_MAP_READ)] HANDLE* pSection);
}
```

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
|-|-|
| Cliente mínimo compatible | Actualización de aniversario de Windows 10 (versión 1607, compilación 14393) |
| Servidor mínimo compatible | Windows Server 2016 (compilación 14393) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Objetos y vistas de la sección](/windows-hardware/drivers/kernel/section-objects-and-views)
</dt> <dt>

[Función **ZwCreateSection** (incluidas las especificaciones de acceso)](/windows-hardware/drivers/ddi/wdm/nf-wdm-zwcreatesection)
</dt> </dl>
