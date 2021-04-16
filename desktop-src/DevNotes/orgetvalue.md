---
description: Recupera el tipo y los datos para el valor del registro especificado en un subárbol del registro sin conexión.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: Función ORGetValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649850"
---
# <a name="orgetvalue-function"></a>ORGetValue función)

Recupera el tipo y los datos para el valor del registro especificado en un subárbol del registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ de de\]
</dt> <dd>

Identificador de una clave del registro abierta en un subárbol del registro sin conexión.

</dd> <dt>

*lpSubKey* \[ en, opcional\]
</dt> <dd>

Nombre de la clave del Registro. Esta clave debe ser una subclave de la clave especificada por el parámetro *Handle* . Este parámetro puede ser **NULL**.

Los nombres de clave no distinguen mayúsculas de minúsculas.

</dd> <dt>

*lpValue* \[ en, opcional\]
</dt> <dd>

Nombre del valor del registro. Si este parámetro es **null** o una cadena vacía, "", la función recupera el tipo y los datos para el valor sin nombre o predeterminado de la clave, si existe. Para obtener más información, vea [límites de tamaño de elementos del registro](../sysinfo/registry-element-size-limits.md).

Las claves no tienen un valor predeterminado o sin nombre. Los valores sin nombre pueden ser de cualquier tipo.

Los nombres de valor no distinguen mayúsculas de minúsculas.

</dd> <dt>

*pdwType* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe un código que indica el tipo de datos almacenados en el valor especificado. Para obtener una lista de los códigos de tipo posibles, vea [Registry Value Types](../sysinfo/registry-value-types.md). Este parámetro puede ser **null** si el tipo no es necesario.

</dd> <dt>

*pvData* \[ out, opcional\]
</dt> <dd>

Un puntero a un búfer que recibe los datos del valor. Este parámetro puede ser **null** si los datos no son necesarios.

Si los datos son una cadena, la función comprueba si hay un carácter nulo de terminación. Si no se encuentra ninguno, la cadena se almacena con un terminador nulo si el búfer es lo suficientemente grande como para alojar el carácter adicional. De lo contrario, se produce un error en la función y se devuelven \_ más \_ datos.

</dd> <dt>

*pcbData* \[ in, out, opcional\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer al que apunta el parámetro *pvData* , en bytes. Cuando la función devuelve, esta variable contiene el tamaño de los datos copiados en *pvData*.

El parámetro *pcbData* solo puede ser **null** si *pvData* es **null**.

Si los datos tienen el \_ tipo REG SZ, REG \_ multi \_ SZ o REG \_ Expand \_ SZ, este tamaño incluye el carácter o caracteres nulos de terminación. Para obtener más información, vea la sección Comentarios.

Si el búfer especificado por el parámetro *pvData* no es lo suficientemente grande como para contener los datos, la función devuelve el error \_ más \_ datos y almacena el tamaño de búfer necesario en la variable a la que apunta *pcbData*. En este caso, el contenido del búfer *pvData* no está definido.

Si *pvData* es **null** y *pcbData* no es **null**, la función devuelve el error \_ Success y almacena el tamaño de los datos, en bytes, en la variable a la que apunta *pcbData*. Esto permite que una aplicación determine la mejor manera de asignar un búfer para los datos del valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.

## <a name="remarks"></a>Observaciones

Una aplicación normalmente llama a la función [**OREnumValue**](orenumvalue.md) para determinar los nombres de valor y, después, llama a la función **ORGetValue** para recuperar los datos de los nombres.

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

[**OREnumValue**](orenumvalue.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
