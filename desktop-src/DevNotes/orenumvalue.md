---
description: Enumera los valores de la clave del registro abierta especificada en un subárbol del registro sin conexión. La función recupera información de un valor en la clave especificada cada vez que se llama a la función.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Función OREnumValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670891"
---
# <a name="orenumvalue-function"></a>OREnumValue función)

Enumera los valores de la clave del registro abierta especificada en un subárbol del registro sin conexión. La función recupera información de un valor en la clave especificada cada vez que se llama a la función.

## <a name="syntax"></a>Sintaxis


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
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

Índice del valor que se va a recuperar. Este parámetro debe ser cero para la primera llamada a la función y, a continuación, incrementarse en las llamadas posteriores.

Dado que los valores no están ordenados, cualquier valor nuevo tendrá un índice arbitrario. Esto significa que la función puede devolver valores en cualquier orden.

</dd> <dt>

*lpValueName* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe el nombre del valor como una cadena terminada en NULL. Este búfer debe ser lo suficientemente grande como para incluir el carácter nulo de terminación.

Para obtener más información, vea [límites de tamaño de elementos del registro](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcValueName* \[ in, out\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer al que apunta el parámetro *lpValueName* , en caracteres. Cuando la función devuelve, la variable recibe el número de caracteres almacenados en el búfer, sin incluir el carácter nulo de terminación.

</dd> <dt>

*lpType* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe un código que indica el tipo de datos almacenados en el valor especificado. Para obtener una lista de los códigos de tipo posibles, vea [Registry Value Types](../sysinfo/registry-value-types.md). El parámetro *lpType* puede ser **null** si no se requiere el código de tipo.

</dd> <dt>

*lpData* \[ out, opcional\]
</dt> <dd>

Un puntero a un búfer que recibe los datos de la entrada de valor. Este parámetro puede ser **null** si los datos no son necesarios.

Si *lpData* es **null** y *lpcbData* no es **null**, la función almacena el tamaño de los datos, en bytes, en la variable a la que apunta *lpcbData*. Esto permite que una aplicación determine la mejor manera de asignar un búfer para los datos.

</dd> <dt>

*lpcbData* \[ in, out, opcional\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer al que apunta el parámetro *lpData* , en bytes. Cuando la función devuelve, la variable recibe el número de bytes almacenados en el búfer.

Este parámetro solo puede ser **null** si *lpData* es **null**.

Si los datos tienen el \_ tipo REG SZ, REG \_ multi \_ SZ o REG \_ Expand \_ SZ, este tamaño incluye el carácter o caracteres nulos de terminación. Para obtener más información, vea la sección Comentarios.

Si el búfer especificado por *lpData* no es lo suficientemente grande como para contener los datos, la función devuelve el error \_ más \_ datos y almacena el tamaño de búfer necesario en la variable a la que apunta *lpcbData*. En este caso, el contenido de *lpData* no está definido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.

Si el búfer de *lpData* es demasiado pequeño para recibir el valor, la función devuelve los datos de error \_ \_ .

## <a name="remarks"></a>Observaciones

Para enumerar los valores, una aplicación debe llamar inicialmente a la función **OREnumValue** con el parámetro *dwIndex* establecido en cero. A continuación, la aplicación debe incrementar *dwIndex* y llamar a la función **OREnumValue** hasta que no haya más valores (hasta que la función devuelva el error \_ no \_ más \_ elementos).

La aplicación también puede establecer *dwIndex* en el índice del último valor de la primera llamada a la función y disminuir el índice hasta que se enumere el valor con el índice 0. Para recuperar el índice del último valor, utilice la función [**ORQueryInfoKey**](orqueryinfokey.md) .

Al utilizar **OREnumValue**, una aplicación no debe llamar a las funciones del registro sin conexión que puedan cambiar la clave que se consulta.

Si los datos tienen el \_ tipo REG SZ, REG \_ multi \_ SZ o REG \_ Expand \_ SZ, es posible que la cadena no se haya almacenado con los caracteres correctos de terminación null. Por lo tanto, aunque la función devuelva el ERROR \_ Success, la aplicación debe asegurarse de que la cadena se termina correctamente antes de usarla; de lo contrario, puede sobrescribir un búfer. (Tenga en cuenta que REG \_ Las \_ cadenas de varios SZ deben tener dos caracteres de terminación null).

Para determinar el tamaño máximo del nombre y los búferes de datos, use la función [**ORQueryInfoKey**](orqueryinfokey.md) .

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

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
