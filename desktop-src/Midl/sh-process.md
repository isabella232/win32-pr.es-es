---
title: Palabra clave sh_process
description: La \_ palabra clave \ SH Process \ especifica que el objeto del sistema es un identificador de un proceso.
keywords:
- palabra clave sh_process MIDL
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3652c6889c687173bbf7b397cddff4659c0329f1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "105721193"
---
# <a name="sh_process-keyword"></a>SH \_ (palabra clave de proceso)

La palabra clave de **\_ proceso SH** especifica que un `system_handle` contiene un identificador de un proceso.

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
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
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
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

[Acerca de los procesos y los subprocesos](../procthread/about-processes-and-threads.md)
</dt> <dt>

[Seguridad del proceso y derechos de acceso](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[**CreateProcess** (función)](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[**OpenProcess** (función)](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>