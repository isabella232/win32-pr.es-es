---
title: Palabra clave sh_pipe
description: La palabra clave \ sh \_ pipe\ especifica que el objeto del sistema es un identificador de una canalización.
keywords:
- sh_pipe clave MIDL
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 15bee0e34525d83af10e5c42199116dc6080a6a7b7f4e2af3de565f62a9c6a5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383350"
---
# <a name="sh_pipe-keyword"></a>Palabra clave \_ sh pipe

La **palabra clave sh \_ pipe** especifica que `system_handle` un contiene un identificador para una canalización.

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
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
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
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

[Acerca de las canalizaciones](../ipc/about-pipes.md)
</dt> <dt>

[Derechos de acceso y seguridad de archivos](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[**Función CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[**Función CreateNamedPipe**](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
