---
description: Convierte una cadena en un GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: Función GUIDFromString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: 38dd6d6365c3b306e63634fee02ac7add07b1bf262598efc88ffec2595e14c82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351065"
---
# <a name="guidfromstring-function"></a>Función GUIDFromString

\[**GUIDFromString** está disponible a través Windows XP con Service Pack 2 (SP2) o Windows Vista. Podría modificarse o no estar disponible en versiones posteriores. Las aplicaciones deben [**usar CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) [**o IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) en lugar de esta función.\]

Convierte una cadena en un GUID.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*psz* \[ En\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a la cadena terminada en NULL que se convertirá. La cadena debe tener el formato siguiente:

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

*pguid* \[ out\]
</dt> <dd>

Tipo: **LPGUID**

Puntero a un búfer para recibir el GUID cuando este método vuelve.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **BOOL**

**TRUE** si el GUID se creó correctamente; de lo contrario, **FALSE**.

## <a name="remarks"></a>Comentarios

Esta función no se declara en un encabezado ni se exporta por nombre desde un .dll archivo. Se debe cargar desde Shell32.dll como ordinal 703 para **GUIDFromStringA** y ordinal 704 para **GUIDFromStringW.**

También se puede acceder a Shlwapi.dll como ordinal 269 para **GUIDFromStringA** y ordinal 270 para **GUIDFromStringW.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **GUIDFromStringW** (Unicode) y **GUIDFromStringA** (ANSI)<br/>                |



 

 
