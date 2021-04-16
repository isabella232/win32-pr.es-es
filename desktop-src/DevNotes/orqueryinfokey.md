---
description: Recupera información acerca de la clave del registro especificada en un subárbol del registro sin conexión.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: Función ORQueryInfoKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671276"
---
# <a name="orqueryinfokey-function"></a>ORQueryInfoKey función)

Recupera información acerca de la clave del registro especificada en un subárbol del registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ de de\]
</dt> <dd>

Identificador de una clave del registro abierta en un subárbol del registro sin conexión.

</dd> <dt>

*lpClass* \[ out, opcional\]
</dt> <dd>

Un puntero a un búfer que recibe la clase clave. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcClass* \[ in, out, opcional\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer al que apunta el parámetro *lpClass* , en caracteres.

El tamaño debe incluir el carácter nulo de terminación. Cuando la función devuelve, esta variable contiene el tamaño de la cadena de clase que se almacena en el búfer. El recuento devuelto no incluye el carácter nulo de terminación. Si el búfer no es suficientemente grande, la función devuelve un ERROR \_ más \_ datos y la variable contiene el tamaño de la cadena, en caracteres, sin contar el carácter null de terminación.

Si *lpClass* es **null**, *lpcClass* puede ser **null**.

Si el parámetro *lpClass* es una dirección válida, pero el parámetro *lpcClass* no es (por ejemplo, si el parámetro *lpcClass* es **null**), la función devuelve un parámetro de error \_ no válido \_ .

</dd> <dt>

*lpcSubKeys* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el número de subclaves que contiene la clave especificada. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcMaxSubKeyLen* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de la subclave de la clave con el nombre más largo, en caracteres Unicode, sin incluir el carácter nulo de terminación. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcMaxClassLen* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de la cadena más larga que especifica una clase de subclave, en caracteres Unicode. El recuento devuelto no incluye el carácter nulo de terminación. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcValues* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el número de valores que están asociados a la clave. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcMaxValueNameLen* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el tamaño del nombre del valor más largo de la clave, en caracteres Unicode. El tamaño no incluye el carácter nulo de terminación. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcMaxValueLen* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el tamaño del componente de datos más largo entre los valores de la clave, en bytes. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcbSecurityDescriptor* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el tamaño del descriptor de seguridad de la clave, en bytes. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpftLastWriteTime* \[ out, opcional\]
</dt> <dd>

Puntero a una estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que recibe la hora de la última escritura. Este parámetro puede ser **NULL**.

La función establece los miembros de la estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para indicar la última vez que se modifica la clave o cualquiera de sus entradas de valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.

Si el búfer de *lpClass* es demasiado pequeño para recibir el nombre de la clase, la función devuelve los datos de error \_ \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows offline Registry Library versión 1,0 o posterior<br/>                      |
| Encabezado<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> </dl>

 

 
