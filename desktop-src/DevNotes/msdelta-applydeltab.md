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
ms.openlocfilehash: 2a6034ca101a192be66db1b16a4ac7b27e7288d9453dfaaab5782e55e11d4c67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079765"
---
# <a name="applydeltab-function"></a>Función ApplyDeltaB

Usa la diferencia y el origen (proporcionados como búferes) para crear una nueva copia de los datos de destino. Los datos de salida se devuelven en un búfer asignado por MSDelta.

> [!NOTE]
> Debe llamar a [DeltaFree para](msdelta-deltafree.md) liberar el búfer de salida una vez completada esta función.

> [!NOTE]
> Si la diferencia especificada se creó mediante [PatchAPI](patchapi.md)y se ha establecido la marca [DELTA_APPLY_FLAG_ALLOW_PA19,](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) MSDelta llamará a PatchAPI para aplicar la diferencia.

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

[in] Puede [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) o [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).

*Origen*

[in] Estructura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contiene un puntero al búfer que contiene los datos de origen.

*Delta*

[in] Estructura [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) que contiene un puntero al búfer que contiene los datos diferenciales.

*lpTarget*

[out] Puntero a la [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) estructura donde se va a escribir el destino.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE** si se realiza correctamente; de lo contrario, devuelve **FALSE**. Cuando la función devuelve **FALSE,** puede llamar a [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obtener el código de error del sistema Win32 correspondiente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Encabezado | msdelta.h |
| Archivo DLL | msdelta.dll |
| Unicode | No aplicable |

## <a name="see-also"></a>Vea también

[MSDelta](msdelta.md)

[DeltaFree](msdelta-deltafree.md)
