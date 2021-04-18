---
title: Palabra clave sh_mutex
description: La \_ palabra clave \ SH mutex \ especifica que el objeto del sistema es un identificador de una exclusión mutua.
keywords:
- palabra clave sh_mutex MIDL
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721387"
---
# <a name="sh_mutex-keyword"></a>SH \_ (palabra clave mutex)

La palabra clave de **\_ exclusión mutua SH** especifica que un `system_handle` contiene un identificador para una exclusión mutua.

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
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
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
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

[Objetos mutex](../sync/mutex-objects.md)
</dt> <dt>

[Derechos de acceso y seguridad de objetos de sincronización](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateMutex** (función)](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[**CreateMutexEx** función)](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>