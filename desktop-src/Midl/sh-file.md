---
title: Palabra clave sh_file
description: La palabra clave \ sh \_ file\ especifica que el objeto del sistema es un identificador de un archivo.
keywords:
- sh_file clave MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 05b76ad772ca628a28677d9b0da06252d0fec70251a4a197d39b50b9760ef931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013633"
---
# <a name="sh_file-keyword"></a>Palabra clave \_ sh file

La **palabra clave sh \_ file** especifica que `system_handle` un contiene un identificador para un archivo.

``` syntax
[system_handle(sh_file)]

[system_handle(sh_file, access-rights)]
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
    HRESULT WriteThisFile([in, system_handle(sh_file)] HANDLE file);

    HRESULT GetFileToRead([out, system_handle(sh_file, READ_CONTROL | SYNCHRONIZE | FILE_READ_DATA | FILE_READ_keywordS | FILE_READ_EA)] HANDLE* pReadThisFile);
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

[Derechos de acceso y seguridad de archivos](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[DirectComposition](/windows/win32/api/_directcomp/)
</dt> <dt>

[**Función DCompositionCreateSurfaceHandle**](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> <dt>
