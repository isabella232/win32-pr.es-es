---
title: Palabra clave sh_thread
description: La palabra clave \ sh \_ thread\ especifica que el objeto del sistema es un identificador de un subproceso.
keywords:
- sh_thread clave MIDL
topic_type:
- apiref
api_name:
- sh_thread keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5cd3f5458e54ccd266f5ef0920b1cc79e1c0b42e35fac51f7ac353d22409aaa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641342"
---
# <a name="sh_thread-keyword"></a>Palabra clave \_ sh thread

La **palabra clave sh \_ thread** especifica que `system_handle` un contiene un identificador para un subproceso.

``` syntax
[system_handle(sh_thread)]

[system_handle(sh_thread, access-rights)]
```

## <a name="parameters"></a>Parámetros

Esta palabra clave es un parámetro para [**system_handle**](system-handle.md).

La [**system_handle**](system-handle.md) documentación también contiene detalles sobre el uso opcional del *parámetro access-rights.* El comportamiento predeterminado es según `DUPLICATE_SAME_ACCESS` las [ **especificaciones de la función DuplicateHandle.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Comentarios

Para usar esta palabra clave con el atributo , la marca debe establecerse en `system_handle` `-target` (o superior) al ejecutar `NT100` midl.exe.

## <a name="examples"></a>Ejemplos

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SetThread([in, system_handle(sh_process)] HANDLE threadHandle);
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

[Acerca de los procesos y los subprocesos](../procthread/about-processes-and-threads.md)
</dt> <dt>

[Derechos de acceso y seguridad de subprocesos](../procthread/thread-security-and-access-rights.md)
</dt> <dt>

[**Función CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
</dt> <dt>

[**Función OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)
</dt> </dl>