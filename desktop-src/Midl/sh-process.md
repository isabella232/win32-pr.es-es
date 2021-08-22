---
title: Palabra clave sh_process
description: La palabra clave \sh \_ process\ especifica que el objeto del sistema es un identificador de un proceso.
keywords:
- sh_process clave MIDL
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3dc11f2980e5124bbc76d0b57fce21d8007b0c09905ca47707d5be6fbb112d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146278"
---
# <a name="sh_process-keyword"></a>Sh \_ process (palabra clave)

La **palabra clave sh \_ process** especifica que contiene `system_handle` un identificador para un proceso.

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
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
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
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

[Acerca de los procesos y los subprocesos](../procthread/about-processes-and-threads.md)
</dt> <dt>

[Derechos de acceso y seguridad de procesos](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[**Función CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[**Función OpenProcess**](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>