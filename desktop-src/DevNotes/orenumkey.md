---
description: Enumera las subclaves de la clave del Registro abierta especificada en un subárbol del Registro sin conexión. La función recupera información sobre una subclave cada vez que se llama a ella.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Función OREnumKey (Offreg.h)
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
ms.openlocfilehash: ab72c9b0df79d464f802a1c574b749d04a8a16e89645f25959681e7f03eea5ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058715"
---
# <a name="orenumkey-function"></a>Función OREnumKey

Enumera las subclaves de la clave del Registro abierta especificada en un subárbol del Registro sin conexión. La función recupera información sobre una subclave cada vez que se llama a ella.

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

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión.

</dd> <dt>

*dwIndex* \[ En\]
</dt> <dd>

Índice de la subclave que se recuperará. Este parámetro debe ser cero para la primera llamada a la función y, a continuación, incrementarse para las llamadas posteriores.

Dado que las subclaves no están ordenadas, cualquier nueva subclave tendrá un índice arbitrario. Esto significa que la función puede devolver subclaves en cualquier orden.

</dd> <dt>

*lpName* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe el nombre de la subclave, incluido el carácter nulo de terminación. La función copia solo el nombre de la subclave, no la jerarquía de claves completa, en el búfer. Si se produce un error en la función, no se copia ninguna información en este búfer.

Para obtener más información, vea [Límites de tamaño de elementos del Registro.](../sysinfo/registry-element-size-limits.md)

</dd> <dt>

*lpcName* \[ in, out\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer especificado por el parámetro *lpName,* en **WCHARs**. Este tamaño debe incluir el carácter nulo de terminación. Si la función se realiza correctamente, la variable a la que apunta *lpcName* contiene el número de caracteres almacenados en el búfer, sin incluir el carácter nulo final.

</dd> <dt>

*lpClass* \[ out, opcional\]
</dt> <dd>

Puntero a un búfer que recibe la cadena de clase terminada en NULL de la subclave enumerada. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcClass* \[ in, out, optional\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer especificado por el parámetro *lpClass,* en **WCHARs**. El tamaño debe incluir el carácter nulo de terminación. Si la función se realiza correctamente, *lpcClass* contiene el número de caracteres almacenados en el búfer, sin incluir el carácter nulo final. Este parámetro solo puede ser **NULL** si *lpClass* es **NULL.**

</dd> <dt>

*lpftLastWriteTime* \[ out, opcional\]
</dt> <dd>

Puntero a la [estructura FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que recibe la hora a la que se escribió por última vez la subclave enumerada. Este parámetro puede ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error. Entre los posibles códigos de error se incluyen los siguientes:

-   Si el *búfer lpName* es demasiado pequeño para recibir el nombre de la clave, la función devuelve ERROR \_ MORE \_ DATA.
-   Si no hay más subclaves disponibles, la función devuelve ERROR \_ NO \_ MORE \_ ITEMS.

## <a name="remarks"></a>Comentarios

Para enumerar subclaves, una aplicación debe llamar inicialmente a la función **OREnumKey** con el parámetro *dwIndex* establecido en cero. A continuación, la aplicación debe incrementar el parámetro *dwIndex* y llamar a **OREnumKey** hasta que no haya más subclaves (lo que significa que la función devuelve ERROR \_ NO MORE \_ \_ ITEMS).

La aplicación también puede establecer *dwIndex* en el índice de la última subclave en la primera llamada a la función y disminuir el índice hasta que se enumera la subclave con el índice 0. Para recuperar el índice de la última subclave, use la [**función ORQueryInfoKey.**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya)

Mientras una aplicación usa la función **OREnumKey,** no debe realizar llamadas a ninguna función del Registro sin conexión que pueda cambiar la clave que se enumera.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca del Registro sin conexión versión 1.0 o posterior<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
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

 

 
