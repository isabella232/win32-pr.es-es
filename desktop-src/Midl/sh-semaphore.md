---
title: Palabra clave sh_semaphore
description: La \_ palabra clave \ SH Semaphore \ especifica que el objeto del sistema es un identificador de un semáforo.
keywords:
- palabra clave sh_semaphore MIDL
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2a5c33e4c44b67e3106a48cde244abaf13f41ad5
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "105721183"
---
# <a name="sh_semaphore-keyword"></a>SH \_ Semaphore (palabra clave)

La palabra clave del **\_ semáforo de SH** especifica que un `system_handle` contiene un identificador de un semáforo.

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
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
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
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

[Objetos Semaphore](../sync/semaphore-objects.md)
</dt> <dt>

[Derechos de acceso y seguridad de objetos de sincronización](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**Createsemaphore (** función)](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[**CreateSemaphoreEx** función)](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
