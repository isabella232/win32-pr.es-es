---
description: Establece los datos para el valor de una clave del Registro especificada en un subárbol del Registro sin conexión.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: Función ORSetValue (Offreg.h)
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
ms.openlocfilehash: ae677a5dff2bcb7189b17c7d1477c95df5a5ae32b0065104b92e426e364d775d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749645"
---
# <a name="orsetvalue-function"></a>Función ORSetValue

Establece los datos para el valor de una clave del Registro especificada en un subárbol del Registro sin conexión.

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

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión.

</dd> <dt>

*lpValueName* \[ en, opcional\]
</dt> <dd>

Nombre del valor que se va a establecer. Si un valor con este nombre aún no está presente en la clave, la función lo agrega a la clave.

Si *lpValueName* es **NULL** o una cadena vacía, "", la función establece el tipo y los datos del valor predeterminado o sin nombre de la clave.

Para obtener más información, vea [Límites de tamaño de elemento del Registro.](../sysinfo/registry-element-size-limits.md)

Las claves del Registro no tienen valores predeterminados, pero pueden tener un valor sin nombre, que puede ser de cualquier tipo.

</dd> <dt>

*dwType* \[ En\]
</dt> <dd>

Tipo de datos al que apunta el *parámetro lpData.* Para obtener una lista de los tipos posibles, vea [Tipos de valor del Registro](../sysinfo/registry-value-types.md).

</dd> <dt>

*lpData* \[ en, opcional\]
</dt> <dd>

Datos que se van a almacenar.

Para los tipos basados en cadenas, como REG \_ SZ, la cadena debe terminar en null. Para el tipo de datos REG \_ MULTI \_ SZ, la cadena debe terminar con dos caracteres NULL.

</dd> <dt>

*cbData* \[ En\]
</dt> <dd>

Tamaño de la información a la que apunta el *parámetro lpData,* en bytes. Si los datos son de tipo REG SZ, REG EXPAND SZ o \_ \_ REG MULTI \_ \_ \_ SZ, *cbData* debe incluir el tamaño del carácter nulo final o de los caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

## <a name="remarks"></a>Comentarios

Los tamaños de valor están limitados por la memoria disponible. Los valores largos (más de 2048 bytes) deben almacenarse como archivos con los nombres de archivo almacenados en el Registro. Esto ayuda a que el registro se realice de forma eficaz. Los elementos de la aplicación, como iconos, mapas de bits y archivos ejecutables, deben almacenarse como archivos y no colocarse en el Registro.

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

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
