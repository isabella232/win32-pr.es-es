---
description: Enumera los valores de la clave del Registro abierta especificada en un subárbol del Registro sin conexión. La función recupera información de un valor bajo la clave especificada cada vez que se llama a la función.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Función OREnumValue (Offreg.h)
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
ms.openlocfilehash: 57a65e8fd862215bd6281e487520857580cf6026b94b2ca375079f84407e4cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331814"
---
# <a name="orenumvalue-function"></a>Función OREnumValue

Enumera los valores de la clave del Registro abierta especificada en un subárbol del Registro sin conexión. La función recupera información de un valor bajo la clave especificada cada vez que se llama a la función.

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

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión.

</dd> <dt>

*dwIndex* \[ En\]
</dt> <dd>

Índice del valor que se va a recuperar. Este parámetro debe ser cero para la primera llamada a la función y, a continuación, incrementarse para las llamadas posteriores.

Dado que los valores no están ordenados, cualquier valor nuevo tendrá un índice arbitrario. Esto significa que la función puede devolver valores en cualquier orden.

</dd> <dt>

*lpValueName* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe el nombre del valor como una cadena terminada en NULL. Este búfer debe ser lo suficientemente grande como para incluir el carácter nulo de terminación.

Para obtener más información, vea [Límites de tamaño de elementos del Registro.](../sysinfo/registry-element-size-limits.md)

</dd> <dt>

*lpcValueName* \[ in, out\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer al que apunta el parámetro *lpValueName,* en caracteres. Cuando la función devuelve un resultado, la variable recibe el número de caracteres almacenados en el búfer, sin incluir el carácter nulo final.

</dd> <dt>

*lpType* \[ out, opcional\]
</dt> <dd>

Puntero a una variable que recibe un código que indica el tipo de datos almacenados en el valor especificado. Para obtener una lista de los códigos de tipo posibles, vea [Tipos de valor del Registro](../sysinfo/registry-value-types.md). El *parámetro lpType* puede ser **NULL si** no se requiere el código de tipo.

</dd> <dt>

*lpData* \[ out, opcional\]
</dt> <dd>

Puntero a un búfer que recibe los datos de la entrada de valor. Este parámetro puede ser **NULL** si los datos no son necesarios.

Si *lpData* es **NULL** y *lpcbData* no es **NULL,** la función almacena el tamaño de los datos, en bytes, en la variable a la que apunta *lpcbData*. Esto permite a una aplicación determinar la mejor manera de asignar un búfer para los datos.

</dd> <dt>

*lpcbData* \[ in, out, optional\]
</dt> <dd>

Puntero a una variable que especifica el tamaño del búfer al que apunta el parámetro *lpData,* en bytes. Cuando la función devuelve un resultado, la variable recibe el número de bytes almacenados en el búfer.

Este parámetro solo puede ser **NULL** si *lpData* es **NULL.**

Si los datos tienen el tipo REG SZ, REG MULTI SZ o REG EXPAND SZ, este tamaño incluye cualquier carácter nulo final \_ \_ o \_ \_ \_ caracteres. Para obtener más información, vea la sección Comentarios.

Si el búfer especificado por *lpData* no es lo suficientemente grande como para contener los datos, la función devuelve ERROR MORE DATA y almacena el tamaño de búfer necesario en la variable a la que apunta \_ \_ *lpcbData*. En este caso, el contenido de *lpData* no está definido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

Si el *búfer lpData* es demasiado pequeño para recibir el valor, la función devuelve ERROR \_ MORE \_ DATA.

## <a name="remarks"></a>Comentarios

Para enumerar valores, una aplicación debe llamar inicialmente a la **función OREnumValue** con el *parámetro dwIndex* establecido en cero. A continuación, la aplicación debe incrementar *dwIndex* y llamar a la función **OREnumValue** hasta que no haya más valores (hasta que la función devuelva ERROR \_ NO MORE \_ \_ ITEMS).

La aplicación también puede establecer *dwIndex* en el índice del último valor en la primera llamada a la función y disminuir el índice hasta que se enumera el valor con el índice 0. Para recuperar el índice del último valor, use la [**función ORQueryInfoKey.**](orqueryinfokey.md)

Al usar **OREnumValue,** una aplicación no debe llamar a ninguna función del Registro sin conexión que pueda cambiar la clave que se está consultando.

Si los datos tienen el tipo REG SZ, REG MULTI SZ o REG EXPAND SZ, es posible que la cadena no se haya almacenado con los caracteres de terminación NULL \_ \_ \_ \_ \_ adecuados. Por lo tanto, incluso si la función devuelve ERROR SUCCESS, la aplicación debe asegurarse de que la cadena finaliza correctamente antes de usarlo; de lo contrario, puede \_ sobrescribir un búfer. (Tenga en cuenta que REG \_ Las cadenas MULTI \_ SZ deben tener dos caracteres de terminación null).

Para determinar el tamaño máximo del nombre y los búferes de datos, use la [**función ORQueryInfoKey.**](orqueryinfokey.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
