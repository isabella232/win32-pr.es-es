---
description: Carga el archivo de Hive del Registro especificado en la memoria y valida el subárbol.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Función OROpenHive (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 86ff3d6ff15b030054d40ca7131e521cedb59ebf20c4942951f0e141f27a2840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076019"
---
# <a name="oropenhive-function"></a>Función OROpenHive

Carga el archivo de Hive del Registro especificado en la memoria y valida el subárbol.

## <a name="syntax"></a>Sintaxis


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpHivePath* \[ En\]
</dt> <dd>

Puntero a una cadena Unicode que especifica el nombre del archivo de Hive del Registro que se va a cargar en la memoria. Puede ser un archivo de Hive que se guardó con la función [**ORSaveHive**](orsavehive.md) o que se creó con las funciones [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) o [RegSaveKeyEx.](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) El archivo debe tener un tamaño inferior a 4 GB y el autor de la llamada debe tener acceso FILE \_ READ \_ DATA al archivo. Para obtener más información, vea [Derechos de acceso y seguridad de archivos.](../fileio/file-security-and-access-rights.md)

</dd> <dt>

*phkResult* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un identificador a la clave raíz del subárbol del Registro sin conexión cargado. Si no se puede abrir el archivo de Hive del Registro o se produce un error en la validación, la función establece este parámetro en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error. Entre los posibles códigos de error se incluyen los siguientes:

-   Si el archivo está vacío o tiene un tamaño superior a 4 GB, la función devuelve ERROR \_ BADDB.
-   Si el autor de la llamada no tiene los derechos de acceso necesarios para abrir el archivo, la función devuelve ERROR \_ ACCESS \_ DENIED.
-   Si se produce un error en la validación del subárbol del Registro, la función devuelve ERROR \_ NOT \_ REGISTRY \_ FILE.

## <a name="remarks"></a>Comentarios

La **función OROpenHive** es la única función del Registro sin conexión que valida un subárbol del Registro. Si se produce un error en la validación, no se realiza ningún intento de reparar el subárbol.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca del Registro sin conexión versión 1.0 o posterior<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
