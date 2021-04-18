---
description: Usa la diferencia y el origen (proporcionados como búferes) para crear una nueva copia de los datos de destino. Los datos de salida se devuelven en un búfer asignado por MSDelta.
title: Función ApplyDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721601"
---
# <a name="applydeltab-function"></a>Función ApplyDeltaB

Usa la diferencia y el origen (proporcionados como búferes) para crear una nueva copia de los datos de destino. Los datos de salida se devuelven en un búfer asignado por MSDelta.

> [!NOTE]
> Debe llamar a [DeltaFree](msdelta-deltafree.md) para liberar el búfer de salida después de que esta función se haya completado.

> [!NOTE]
> Si el Delta especificado se creó con [PatchAPI](patchapi.md)y se establece la marca [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , MSDelta llamará a PatchAPI para aplicar la diferencia.

## <a name="syntax"></a>Sintaxis

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a>Parámetros

*ApplyFlags*

de [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) o [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).

*Origen*

de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) estructura que contiene un puntero al búfer que contiene los datos de origen.

*Delta*

de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) estructura que contiene un puntero al búfer que contiene los datos Delta.

*lpTarget*

enuncia Puntero a la estructura de [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) en la que se va a escribir el destino.

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

[DeltaFree](msdelta-deltafree.md)
