---
description: Crea una diferencia entre el origen y el destino (proporcionados como búferes) y devuelve el delta de salida como un búfer asignado por MSDelta.
title: Función CreateDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721577"
---
# <a name="createdeltab-function"></a>Función CreateDeltaB

Crea una diferencia entre el origen y el destino (proporcionados como búferes) y devuelve el delta de salida como un búfer asignado por MSDelta.

> [!NOTE]
> Debe llamar a [DeltaFree](msdelta-deltafree.md) para liberar el búfer de salida después de que esta función se haya completado.

## <a name="syntax"></a>Sintaxis

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a>Parámetros

*FileTypeSet*

de El valor de [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) que indica el tipo de archivo que se va a utilizar para el proceso de creación.

*SetFlags*

de Uno o más valores de [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) que especifican las marcas que se van a utilizar durante el proceso de creación, además de las marcas predeterminadas.

*ResetFlags*

de Uno o más valores de [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) que especifican las marcas predeterminadas que se restablecerán durante el proceso de creación.

*Origen*

de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) estructura que contiene un puntero al búfer que contiene los datos de origen.

*Target*

de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) estructura que contiene un puntero al búfer que contiene los datos de destino.

*SourceOptions*

[in] Reservado. Pase una estructura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con el valor *editable* establecido en **false**, *lpStart* establecido en **null** y *uSize* establecido en 0.

*TargetOptions*

[in] Reservado. Pase una estructura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con el valor *editable* establecido en **false**, *lpStart* establecido en **null** y *uSize* establecido en 0.

*GlobalOptions*

[in] Reservado. Pase una estructura de [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) con *LpStart* establecido en **null** y *uSize* establecido en 0.

*lpTargetFileTime*

de La marca de tiempo establecida en el archivo de destino después de aplicar la diferencia. Si **es null**, la marca de tiempo de destino será la hora actual durante el proceso de creación.

*HashAlgId*

de ALG_ID del algoritmo que se va a utilizar para generar la firma de destino. Algunos valores especiales son:

- 0 = sin signatura
- 32 = CRC de 32 bits definido en msdelta.dll

*lpDelta*

enuncia Puntero a la estructura de [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) en la que se va a escribir la diferencia.

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
