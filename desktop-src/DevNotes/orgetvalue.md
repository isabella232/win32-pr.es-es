---
description: Recupera el tipo y los datos del valor del Registro especificado en un subárbol del Registro sin conexión.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: Función ORGetValue (Offreg.h)
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
ms.openlocfilehash: fc364e208e9c243754edf8731f077ec48e9133d4a95ba86b5a1f99971192b51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058655"
---
# <a name="orgetvalue-function"></a>Función ORGetValue

Recupera el tipo y los datos del valor del Registro especificado en un subárbol del Registro sin conexión.

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

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión.

</dd> <dt>

*lpSubKey* \[ en, opcional\]
</dt> <dd>

Nombre de la clave del Registro. Esta clave debe ser una subclave de la clave especificada por el *parámetro Handle.* Este parámetro puede ser **NULL**.

Los nombres de clave no distinguen mayúsculas de minúsculas.

</dd> <dt>

*lpValue* \[ en, opcional\]
</dt> <dd>

Nombre del valor del Registro. Si este parámetro es **NULL** o una cadena vacía, "", la función recupera el tipo y los datos del valor predeterminado o sin nombre de la clave, si existe. Para obtener más información, vea [Límites de tamaño de elemento del Registro.](../sysinfo/registry-element-size-limits.md)

Las claves no tienen automáticamente un valor sin nombre o predeterminado. Los valores sin nombre pueden ser de cualquier tipo.

Los nombres de valor no distinguen mayúsculas de minúsculas.

</dd> <dt>

*pdwType* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe un código que indica el tipo de datos almacenados en el valor especificado. Para obtener una lista de los códigos de tipo posibles, vea [Tipos de valor del Registro](../sysinfo/registry-value-types.md). Este parámetro puede ser **NULL** si el tipo no es necesario.

</dd> <dt>

*pvData* \[ out, opcional\]
</dt> <dd>

Puntero a un búfer que recibe los datos del valor. Este parámetro puede ser **NULL** si los datos no son necesarios.

Si los datos son una cadena, la función comprueba si hay un carácter nulo de terminación. Si no se encuentra una, la cadena se almacena con un terminador null si el búfer es lo suficientemente grande como para dar cabida al carácter adicional. De lo contrario, se produce un error en la función y devuelve ERROR \_ MORE \_ DATA.

</dd> <dt>

*pwData* \[ in, out, optional\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer al que apunta el *parámetro pvData,* en bytes. Cuando la función vuelve, esta variable contiene el tamaño de los datos copiados en *pvData.*

El *parámetro typeData* solo puede **ser NULL** si *pvData* es **NULL.**

Si los datos tienen el tipo REG SZ, REG MULTI SZ o REG EXPAND SZ, este tamaño incluye cualquier carácter o carácter \_ \_ nulo \_ \_ \_ final. Para obtener más información, vea la sección Comentarios.

Si el búfer especificado por el parámetro *pvData* no es lo suficientemente grande como para contener los datos, la función devuelve ERROR MORE DATA y almacena el tamaño de búfer necesario en la variable a la que \_ \_ *apuntan los datos de .* En este caso, el contenido del búfer *pvData* no está definido.

Si *pvData* es **NULL** y *byteData* no es **NULL,** la función devuelve ERROR SUCCESS y almacena el tamaño de los datos, en bytes, en la variable a la que \_ apunta *byteData*. Esto permite a una aplicación determinar la mejor manera de asignar un búfer para los datos del valor.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

## <a name="remarks"></a>Comentarios

Normalmente, una aplicación llama a la [**función OREnumValue**](orenumvalue.md) para determinar los nombres de valor y, a continuación, llama a la **función ORGetValue** para recuperar los datos de los nombres.

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

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OREnumValue**](orenumvalue.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
