---
description: Carga el archivo de subárbol del registro especificado en la memoria y valida el subárbol.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Función OROpenHive (Offreg. h)
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
ms.openlocfilehash: ba6531e7a2ab2b0b148065d9f4666812e75f2968
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671346"
---
# <a name="oropenhive-function"></a>OROpenHive función)

Carga el archivo de subárbol del registro especificado en la memoria y valida el subárbol.

## <a name="syntax"></a>Sintaxis


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpHivePath* \[ de\]
</dt> <dd>

Puntero a una cadena Unicode que especifica el nombre del archivo de subárbol del registro que se va a cargar en la memoria. Puede tratarse de un archivo de Hive que se guardó con la función [**ORSaveHive**](orsavehive.md) o que se creó con la función [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) o [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) . El archivo debe tener un tamaño inferior a 4 GB y el llamador debe tener acceso de \_ datos de lectura de archivos \_ al archivo. Para obtener más información, vea [seguridad de archivos y derechos de acceso](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*phkResult* \[ enuncia\]
</dt> <dd>

Un puntero a una variable que recibe un identificador a la clave raíz del subárbol del registro cargado sin conexión. Si no se puede abrir el archivo de subárbol del registro o se produce un error en la validación, la función establece este parámetro en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error. Entre los posibles códigos de error se incluyen los siguientes:

-   Si el archivo está vacío o tiene un tamaño superior a 4 GB, la función devuelve el ERROR \_ BADDB.
-   Si el llamador no tiene los derechos de acceso necesarios para abrir el archivo, la función devuelve el ERROR \_ acceso \_ denegado.
-   Si se produce un error en la validación del subárbol del registro, la función devuelve el ERROR \_ no \_ archivo de registro \_ .

## <a name="remarks"></a>Observaciones

La función **OROpenHive** es la única función de registro sin conexión que valida un subárbol del registro. Si se produce un error en la validación, no se realiza ningún intento para reparar el subárbol.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows offline Registry Library versión 1,0 o posterior<br/>                      |
| Encabezado<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
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

 

 
