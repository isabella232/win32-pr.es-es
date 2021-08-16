---
title: Palabra clave sh_semaphore
description: La palabra clave \sh \_ semaphore\ especifica que el objeto del sistema es un identificador para un semáforo.
keywords:
- sh_semaphore clave MIDL
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a48d0b085f3653679c7399ad0f234e7b7a1ecf1b1532480c003923967ac4830a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383225"
---
# <a name="sh_semaphore-keyword"></a>Sh \_ semaphore (palabra clave)

La **palabra clave sh \_ semaphore** especifica que un contiene `system_handle` un identificador para un semáforo.

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
```

## <a name="parameters"></a>Parámetros

Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).

La [**system_handle**](system-handle.md) de acceso también contiene detalles sobre el uso opcional del *parámetro access-rights.* El comportamiento predeterminado es según `DUPLICATE_SAME_ACCESS` las [ **especificaciones de la función DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Comentarios

Para usar esta palabra clave con el atributo , la marca debe establecerse en `system_handle` `-target` `NT100` (o superior) al ejecutar midl.exe.

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
| Cliente mínimo compatible | Windows 10 Actualización de aniversario (versión 1607, compilación 14393) |
| Servidor mínimo compatible | Windows Server 2016 (compilación 14393) |

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Objetos semáforos](../sync/semaphore-objects.md)
</dt> <dt>

[Derechos de acceso y seguridad de objetos de sincronización](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**Función CreateSemaphore**](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[**Función CreateSemaphoreEx**](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
