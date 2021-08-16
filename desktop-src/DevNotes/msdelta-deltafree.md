---
description: Libera el bloque de memoria especificado.
title: Función DeltaFree
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 606b8d91d20c74f7dd56ff4e09986abec3eef547989990a38bd8b4e3a27382c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079735"
---
# <a name="deltafree-function"></a>Función DeltaFree

Libera el bloque de memoria especificado. Debe llamar a esta función después de llamar correctamente a [CreateDeltaB](msdelta-createdeltab.md) y [ApplyDeltaB](msdelta-applydeltab.md) para liberar el búfer de memoria asignado a MSDelta.

## <a name="syntax"></a>Sintaxis

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a>Parámetros

*lpMemory*

[in] Bloque de memoria que se va a liberar.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE** si se realiza correctamente; de lo contrario, devuelve **FALSE**. Cuando la función devuelve **FALSE,** puede llamar a [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener el código de error del sistema Win32 correspondiente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Encabezado | msdelta.h |
| Archivo DLL | msdelta.dll |
| Unicode | No aplicable |

## <a name="see-also"></a>Consulte también

[MSDelta](msdelta.md)

[CreateDeltaB](msdelta-createdeltab.md)

[ApplyDeltaB](msdelta-applydeltab.md)
