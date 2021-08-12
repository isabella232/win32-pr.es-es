---
description: Abre la clave del Registro especificada en un subárbol del Registro sin conexión.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: Función OROpenKey (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4c0f641925fbc35fba6072ee395f67fad540dcd2ec5198b945ad658a723238b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667115"
---
# <a name="oropenkey-function"></a>Función OROpenKey

Abre la clave del Registro especificada en un subárbol del Registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión.

</dd> <dt>

*lpSubKeyName* \[ in, opcional\]
</dt> <dd>

Puntero a una cadena UNICODE que contiene el nombre de la clave del Registro que se va a abrir. Esta clave debe ser una subclave de la clave identificada por el *parámetro Handle.*

Los nombres de clave no distinguen mayúsculas de minúsculas.

Si este parámetro es **NULL o** un puntero a una cadena vacía, la función devuelve el mismo identificador que se pasó. Si la clave especificada por el parámetro *Handle* es la clave raíz del subárbol, la función devuelve ERROR \_ INVALID \_ PARAMETER.

Para obtener más información, vea [Límites de tamaño de elementos del Registro.](../sysinfo/registry-element-size-limits.md)

</dd> <dt>

*phkResult* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un identificador para la clave abierta. Use la [**función ORCloseKey**](orclosekey.md) para cerrar la clave una vez que haya terminado de usar el identificador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

Si el identificador que se va a devolver sería un identificador de la clave raíz del subárbol, la función devuelve ERROR \_ INVALID \_ PARAMETER.

Si la clave especificada se ha marcado como eliminada, esta función devuelve ERROR \_ KEY \_ DELETED.

## <a name="remarks"></a>Observaciones

La **función OROpenKey** no se puede usar para abrir la clave raíz en un subárbol del Registro sin conexión. Para obtener un identificador para la clave raíz de un subárbol, use la [**función OROpenHive**](oropenhive.md) para cargar el subárbol en la memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca del Registro sin conexión versión 1.0 o posterior<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
