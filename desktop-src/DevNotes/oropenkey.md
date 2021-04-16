---
description: Abre la clave del registro especificada en un subárbol del registro sin conexión.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: Función OROpenKey (Offreg. h)
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
ms.openlocfilehash: 4a55bb2c06d8b2d13491b766bf08184631fa2164
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650037"
---
# <a name="oropenkey-function"></a>OROpenKey función)

Abre la clave del registro especificada en un subárbol del registro sin conexión.

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

*Identificador* \[ de de\]
</dt> <dd>

Identificador de una clave del registro abierta en un subárbol del registro sin conexión.

</dd> <dt>

*lpSubKeyName* \[ en, opcional\]
</dt> <dd>

Puntero a una cadena Unicode que contiene el nombre de la clave del registro que se va a abrir. Esta clave debe ser una subclave de la clave identificada por el parámetro de *identificador* .

Los nombres de clave no distinguen mayúsculas de minúsculas.

Si este parámetro es **null** o un puntero a una cadena vacía, la función devuelve el mismo identificador que se pasó. Si la clave especificada por el parámetro *Handle* es la clave raíz del subárbol, la función devuelve un \_ parámetro de error no válido \_ .

Para obtener más información, vea [límites de tamaño de elementos del registro](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*phkResult* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe un identificador de la clave abierta. Utilice la función [**ORCloseKey**](orclosekey.md) para cerrar la clave después de haber terminado de usar el identificador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.

Si el identificador que se va a devolver sería un identificador de la clave raíz del subárbol, la función devuelve un parámetro de ERROR \_ no válido \_ .

Si la clave especificada se ha marcado como eliminada, esta función devuelve la clave de ERROR \_ \_ eliminada.

## <a name="remarks"></a>Observaciones

No se puede usar la función **OROpenKey** para abrir la clave raíz en un subárbol del registro sin conexión. Para obtener un identificador de la clave raíz de un subárbol, use la función [**OROpenHive**](oropenhive.md) para cargar el subárbol en la memoria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows offline Registry Library versión 1,0 o posterior<br/>                      |
| Encabezado<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
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

 

 
