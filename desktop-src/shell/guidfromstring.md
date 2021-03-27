---
description: Convierte una cadena en un GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: GUIDFromString (función)
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
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909557"
---
# <a name="guidfromstring-function"></a>GUIDFromString (función)

\[**GUIDFromString** está disponible a través de Windows XP con Service Pack 2 (SP2) o Windows Vista. Podría modificarse o no estar disponible en versiones posteriores. Las aplicaciones deben usar [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) o [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) en lugar de esta función.\]

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

*PSZ* \[ de\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a la cadena terminada en null que se va a convertir. La cadena debe tener el formato siguiente:

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

*pguid* \[ enuncia\]
</dt> <dd>

Tipo: **LPGUID**

Puntero a un búfer para recibir el GUID cuando este método devuelve.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

**True** si el GUID se creó correctamente; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

Esta función no está declarada en un encabezado o exportada por el nombre de un archivo. dll. Se debe cargar desde Shell32.dll como ordinal 703 para **GUIDFromStringA** y el ordinal 704 para **GUIDFromStringW**.

También se puede acceder a él desde Shlwapi.dll como ordinal 269 para **GUIDFromStringA** y el ordinal 270 para **GUIDFromStringW**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **GUIDFromStringW** (Unicode) y **GUIDFromStringA** (ANSI)<br/>                |



 

 
