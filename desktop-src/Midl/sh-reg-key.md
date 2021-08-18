---
title: Palabra clave sh_reg_key
description: La palabra clave \sh \_ reg \_ key\ especifica que el objeto del sistema es un identificador de una clave del Registro.
keywords:
- sh_reg_key clave MIDL
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 321745879645f3f6346d1e4c5ba7047df203430041f2d8903b8ff506229bb1e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013613"
---
# <a name="sh_reg_key-keyword"></a>Sh \_ reg \_ key (palabra clave)

La **palabra clave sh reg \_ \_ key** especifica que contiene `system_handle` un identificador para una clave del Registro.

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
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
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
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

[Registro](../sysinfo/registry.md)
</dt> <dt>

[Derechos de acceso y seguridad de la clave del Registro](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[**Función RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
