---
description: Crea una diferencia entre el archivo de código fuente especificado y el archivo de destino especificado.
title: CreatePatchFileExA/W (función)
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: c84be2d859a780e46e7e940aa4a7e7da5296f0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721575"
---
# <a name="createpatchfileexaw-function"></a>CreatePatchFileExA/W (función)

Las funciones **CreatePatchFileExA** y **CreatePatchFileExW** crean una diferencia entre el archivo de código fuente especificado y el archivo de destino especificado. Los archivos de origen y de destino se proporcionan como rutas de acceso. El delta de salida también se escribe en una ruta de acceso proporcionada. Estas funciones proporcionan informes de progreso durante el proceso de creación.

## <a name="syntax"></a>Sintaxis

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a>Parámetros

*OldFileCount*

Número total de archivos de código fuente. Se usa para crear diferencias en varios archivos de código fuente (255 como máximo).

*OldFileInfoArray*

Puntero a la matriz de información del archivo de código fuente.

*NewFileName*

Nombre del archivo de destino.

*PatchFileName*

Nombre del delta que se crea.

*OptionFlags*

Marcas de creación.

*ProgressCallback*

Puntero a una devolución de llamada de progreso definida por la aplicación.

*CallbackContext*

Puntero a un contexto definido por la aplicación.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Encabezado | patchapi. h |
| Archivo DLL | mspatchc.dll |
| Unicode | Se implementa como CreatePatchFileExW (Unicode) y CreatePatchFileExA (ANSI) |

## <a name="see-also"></a>Vea también

[PatchAPI](patchapi.md)
