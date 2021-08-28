---
title: Palabra clave sh_event
description: La palabra clave \sh \_ event\ especifica que el objeto del sistema es un identificador de un evento.
keywords:
- sh_event clave MIDL
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: b2f489c27d32c40f80cef326b99131158df92cad2183cee1dc5a3dd74310cf6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013653"
---
# <a name="sh_event-keyword"></a>Palabra clave \_ de evento sh

La **palabra clave sh \_ event** especifica que contiene `system_handle` un identificador para un evento.

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
```

## <a name="parameters"></a>Parámetros

Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).

La [**system_handle**](system-handle.md) documentación también contiene detalles sobre el uso opcional del *parámetro access-rights.* El comportamiento predeterminado es según `DUPLICATE_SAME_ACCESS` las especificaciones [ **de la función DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Comentarios

Para usar esta palabra clave con el atributo , la marca debe establecerse en `system_handle` `-target` (o superior) al ejecutar `NT100` midl.exe.

## <a name="examples"></a>Ejemplos

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
}
```

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
|-|-|
| Cliente mínimo compatible | Windows 10 Actualización de aniversario (versión 1607, compilación 14393) |
| Servidor mínimo compatible | Windows Server 2016 (compilación 14393) |

## <a name="see-also"></a>Vea también

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Objetos de evento](../sync/event-objects.md)
</dt> <dt>

[Derechos de acceso y seguridad de objetos de sincronización](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**Función CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**Función CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
