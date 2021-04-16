---
description: Establece los datos para el valor de una clave del registro especificada en un subárbol del registro sin conexión.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: Función ORSetValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650159"
---
# <a name="orsetvalue-function"></a>ORSetValue función)

Establece los datos para el valor de una clave del registro especificada en un subárbol del registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ de de\]
</dt> <dd>

Identificador de una clave del registro abierta en un subárbol del registro sin conexión.

</dd> <dt>

*lpValueName* \[ en, opcional\]
</dt> <dd>

Nombre del valor que se va a establecer. Si un valor con este nombre no está ya presente en la clave, la función lo agrega a la clave.

Si *lpValueName* es **null** o una cadena vacía, "", la función establece el tipo y los datos para el valor sin nombre o predeterminado de la clave.

Para obtener más información, vea [límites de tamaño de elementos del registro](../sysinfo/registry-element-size-limits.md).

Las claves del registro no tienen valores predeterminados, pero pueden tener un valor sin nombre, que puede ser de cualquier tipo.

</dd> <dt>

*dwType* \[ de\]
</dt> <dd>

El tipo de datos al que apunta el parámetro *lpData* . Para obtener una lista de los tipos posibles, vea [Registry Value Types](../sysinfo/registry-value-types.md).

</dd> <dt>

*lpData* \[ en, opcional\]
</dt> <dd>

Datos que se van a almacenar.

En el caso de los tipos basados en cadena, como REG \_ SZ, la cadena debe terminar en NULL. En el caso del \_ tipo de datos reg multi \_ SZ, la cadena debe terminar con dos caracteres null.

</dd> <dt>

*cbData* \[ de\]
</dt> <dd>

Tamaño de la información a la que apunta el parámetro *lpData* , en bytes. Si los datos son del tipo REG \_ SZ, REG \_ Expand \_ SZ o REG \_ multi \_ SZ, *cbData* debe incluir el tamaño del carácter o caracteres nulos de terminación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.

## <a name="remarks"></a>Observaciones

Los tamaños de valor están limitados por la memoria disponible. Los valores largos (más de 2048 bytes) deben almacenarse como archivos con los nombres de archivo almacenados en el registro. Esto ayuda a que el registro funcione de forma eficaz. Los elementos de la aplicación como iconos, mapas de bits y archivos ejecutables deben almacenarse como archivos y no colocarse en el registro.

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

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
