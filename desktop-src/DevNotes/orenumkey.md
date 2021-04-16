---
description: Enumera las subclaves de la clave del registro abierta especificada en un subárbol del registro sin conexión. La función recupera información sobre una subclave cada vez que se llama.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Función OREnumKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649982"
---
# <a name="orenumkey-function"></a>OREnumKey función)

Enumera las subclaves de la clave del registro abierta especificada en un subárbol del registro sin conexión. La función recupera información sobre una subclave cada vez que se llama.

## <a name="syntax"></a>Sintaxis


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ de de\]
</dt> <dd>

Identificador de una clave del registro abierta en un subárbol del registro sin conexión.

</dd> <dt>

*dwIndex* \[ de\]
</dt> <dd>

Índice de la subclave que se va a recuperar. Este parámetro debe ser cero para la primera llamada a la función y, a continuación, incrementarse en las llamadas posteriores.

Dado que las subclaves no están ordenadas, cualquier subclave nueva tendrá un índice arbitrario. Esto significa que la función puede devolver subclaves en cualquier orden.

</dd> <dt>

*lpName* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe el nombre de la subclave, incluido el carácter nulo de terminación. La función copia solo el nombre de la subclave, no la jerarquía de claves completa, en el búfer. Si se produce un error en la función, no se copia ninguna información en este búfer.

Para obtener más información, vea [límites de tamaño de elementos del registro](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcName* \[ in, out\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer especificado por el parámetro *lpName* en **WCHARs**. Este tamaño debe incluir el carácter nulo de terminación. Si la función se ejecuta correctamente, la variable a la que apunta *lpcName* contiene el número de caracteres almacenados en el búfer, sin incluir el carácter nulo de terminación.

</dd> <dt>

*lpClass* \[ out, opcional\]
</dt> <dd>

Un puntero a un búfer que recibe la cadena de clase terminada en NULL de la subclave enumerada. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcClass* \[ in, out, opcional\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer especificado por el parámetro *lpClass* en **WCHARs**. El tamaño debe incluir el carácter nulo de terminación. Si la función se ejecuta correctamente, *lpcClass* contiene el número de caracteres almacenados en el búfer, sin incluir el carácter nulo de terminación. Este parámetro solo puede ser **null** si *lpClass* es **null**.

</dd> <dt>

*lpftLastWriteTime* \[ out, opcional\]
</dt> <dd>

Puntero a la estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que recibe la hora a la que se escribió por última vez en la subclave enumerada. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error. Entre los posibles códigos de error se incluyen los siguientes:

-   Si el búfer de *lpName* es demasiado pequeño para recibir el nombre de la clave, la función devuelve los datos de error \_ \_ .
-   Si no hay más subclaves disponibles, la función devuelve el ERROR \_ no hay \_ más \_ elementos.

## <a name="remarks"></a>Observaciones

Para enumerar las subclaves, una aplicación debe llamar inicialmente a la función **OREnumKey** con el parámetro *dwIndex* establecido en cero. A continuación, la aplicación debe incrementar el parámetro *dwIndex* y llamar a **OREnumKey** hasta que no haya más subclaves (lo que significa que la función devuelve el error \_ no hay \_ más \_ elementos).

La aplicación también puede establecer *dwIndex* en el índice de la última subclave de la primera llamada a la función y disminuir el índice hasta que se Enumere la subclave con el índice 0. Para recuperar el índice de la última subclave, utilice la función [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) .

Mientras una aplicación utiliza la función **OREnumKey** , no debe realizar llamadas a las funciones del registro sin conexión que podrían cambiar la clave que se está enumerando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows offline Registry Library versión 1,0 o posterior<br/>                      |
| Encabezado<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
