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
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721599"
---
# <a name="deltafree-function"></a>Función DeltaFree

Libera el bloque de memoria especificado. Debe llamar a esta función después de las llamadas correctas a [CreateDeltaB](msdelta-createdeltab.md) y [ApplyDeltaB](msdelta-applydeltab.md) para liberar el búfer de memoria asignado a MSDelta.

## <a name="syntax"></a>Sintaxis

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a>Parámetros

*lpMemory*

de Bloque de memoria que se va a liberar.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**. Cuando la función devuelve **false**, puede llamar a [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener el código de error del sistema Win32 correspondiente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Encabezado | msdelta. h |
| Archivo DLL | msdelta.dll |
| Unicode | No aplicable |

## <a name="see-also"></a>Vea también

[MSDelta](msdelta.md)

[CreateDeltaB](msdelta-createdeltab.md)

[ApplyDeltaB](msdelta-applydeltab.md)
