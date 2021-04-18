---
description: Extrae la información de encabezado de un delta.
title: ExtractPatchHeaderToFileA/W (función)
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
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721595"
---
# <a name="extractpatchheadertofileaw-function"></a>ExtractPatchHeaderToFileA/W (función)

Las funciones **ExtractPatchHeaderToFileA** y **ExtractPatchHeaderToFileW** extraen la información de encabezado de un delta. La diferencia se proporciona como una ruta de acceso de archivo. El encabezado de salida también se escribe en una ruta de acceso proporcionada.

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

Nombre del delta que contiene el encabezado.

*PatchHeaderFileName*

Nombre del archivo de encabezado que se va a crear.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|----------------|---------------------------------------------------------------------------------------|
| Encabezado | patchapi. h |
| Archivo DLL | mspatchc.dll |
| Unicode | Se implementa como ExtractPatchHeaderToFileW (Unicode) y ExtractPatchHeaderToFileA (ANSI) |

## <a name="see-also"></a>Vea también

[PatchAPI](patchapi.md)
