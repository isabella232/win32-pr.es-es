---
description: Extrae la información de encabezado de una diferencia.
title: Función ExtractPatchHeaderToFileA/W
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 626bd53e3361f4d29cc76e17ae2788ddea3bc8b99b580196bcbf77c27a6983d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571805"
---
# <a name="extractpatchheadertofileaw-function"></a>Función ExtractPatchHeaderToFileA/W

Las **funciones ExtractPatchHeaderToFileA** **y ExtractPatchHeaderToFileW** extraen la información de encabezado de una diferencia. La diferencia se proporciona como una ruta de acceso de archivo. El encabezado de salida también se escribe en una ruta de acceso proporcionada.

## <a name="syntax"></a>Sintaxis

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a>Parámetros

*PatchFileName*

Nombre de la diferencia que contiene el encabezado.

*PatchHeaderFileName*

Nombre del archivo de encabezado que se va a crear.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **TRUE** si se realiza correctamente; de lo contrario, devuelve **FALSE**.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Encabezado | patchapi.h |
| Archivo DLL | mspatchc.dll |
| Unicode | Se implementa como ExtractPatchHeaderToFileW (Unicode) y ExtractPatchHeaderToFileA (ANSI) |

## <a name="see-also"></a>Vea también

[PatchAPI](patchapi.md)
