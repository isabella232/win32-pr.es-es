---
description: Crea una diferencia entre el archivo de origen especificado y el archivo de destino especificado.
title: Función CreatePatchFileExA/W
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
ms.openlocfilehash: 7d73b6f4d10c52e9eca147227fdbfece31cba157af84fdf56dbef5cacda516b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690875"
---
# <a name="createpatchfileexaw-function"></a>Función CreatePatchFileExA/W

Las **funciones CreatePatchFileExA** y **CreatePatchFileExW** crean una diferencia entre el archivo de origen especificado y el archivo de destino especificado. Los archivos de origen y de destino se proporcionan como rutas de acceso. La diferencia de salida también se escribe en una ruta de acceso proporcionada. Estas funciones proporcionan informes de progreso durante el proceso de creación.

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

Número total de archivos de origen. Se usa para crear diferencias en varios archivos de código fuente (255 como máximo).

*OldFileInfoArray*

Puntero a la matriz de información del archivo de origen.

*NewFileName*

Nombre del archivo de destino.

*PatchFileName*

Nombre de la diferencia que se crea.

*OptionFlags*

Marcas de creación.

*ProgressCallback*

Puntero a la devolución de llamada de progreso definida por la aplicación.

*CallbackContext*

Puntero al contexto definido por la aplicación.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE** si se realiza correctamente; de lo contrario, devuelve **FALSE**.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Encabezado | patchapi.h |
| Archivo DLL | mspatchc.dll |
| Unicode | Se implementa como CreatePatchFileExW (Unicode) y CreatePatchFileExA (ANSI) |

## <a name="see-also"></a>Vea también

[PatchAPI](patchapi.md)
