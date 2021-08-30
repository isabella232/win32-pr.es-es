---
description: Recupera información sobre la clave del Registro especificada en un subárbol del Registro sin conexión.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: Función ORQueryInfoKey (Offreg.h)
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
ms.openlocfilehash: bb7bf6d4a9440e648844e6e18d9b4965b0240de98f8f27f4aac142276142515b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058615"
---
# <a name="orqueryinfokey-function"></a>Función ORQueryInfoKey

Recupera información sobre la clave del Registro especificada en un subárbol del Registro sin conexión.

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

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión.

</dd> <dt>

*lpClass* \[ out, opcional\]
</dt> <dd>

Puntero a un búfer que recibe la clase de clave. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcClass* \[ in, out, optional\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer al que apunta el parámetro *lpClass,* en caracteres.

El tamaño debe incluir el carácter nulo de terminación. Cuando la función vuelve, esta variable contiene el tamaño de la cadena de clase que se almacena en el búfer. El recuento devuelto no incluye el carácter nulo de terminación. Si el búfer no es lo suficientemente grande, la función devuelve ERROR MORE DATA y la variable contiene el tamaño de la cadena, en caracteres, sin contar el carácter \_ \_ nulo final.

Si *lpClass* es **NULL,** *lpcClass* puede ser **NULL.**

Si el *parámetro lpClass* es una dirección válida, pero el parámetro *lpcClass* no es (por ejemplo, si el parámetro *lpcClass* es **NULL),** la función devuelve ERROR \_ INVALID \_ PARAMETER.

</dd> <dt>

*lpcSubKeys* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el número de subclaves que contiene la clave especificada. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcMaxSubKeyLen* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de la subclave de la clave con el nombre más largo, en caracteres Unicode, sin incluir el carácter nulo final. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcMaxClassLen* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de la cadena más larga que especifica una clase de subclave, en caracteres Unicode. El recuento devuelto no incluye el carácter nulo de terminación. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcValues* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el número de valores asociados a la clave. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcMaxValueNameLen* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe el tamaño del nombre de valor más largo de la clave, en caracteres Unicode. El tamaño no incluye el carácter nulo de terminación. Este parámetro puede ser **NULL**.

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

Puntero a una [estructura FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que recibe la hora de la última escritura. Este parámetro puede ser **NULL**.

La función establece los miembros de la [estructura FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para indicar la última vez que se modifica la clave o cualquiera de sus entradas de valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

Si el *búfer lpClass* es demasiado pequeño para recibir el nombre de la clase , la función devuelve ERROR \_ MORE \_ DATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca del Registro sin conexión versión 1.0 o posterior<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
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

 

 
