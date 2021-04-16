---
description: Elimina una subclave y sus valores de un subárbol del registro sin conexión.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Función ORDeleteKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650094"
---
# <a name="ordeletekey-function"></a>ORDeleteKey función)

Elimina una subclave y sus valores de un subárbol del registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ de de\]
</dt> <dd>

Identificador de una clave del registro abierta en un subárbol del registro sin conexión. Este identificador es devuelto por la función [**ORCreateKey**](orcreatekey.md) o [**OROpenKey**](oropenkey.md) .

</dd> <dt>

*lpSubKey* \[ en, opcional\]
</dt> <dd>

Nombre de la clave que se va a eliminar. Debe ser una subclave de la clave que *controla* las identificaciones, pero no puede tener subclaves.

Si la subclave no existe, la función devuelve un ERROR \_ no \_ encontrado.

Si este parámetro es **null**, la función elimina la clave especificada por el parámetro *Handle* . Si la clave especificada por el parámetro *Handle* es la clave raíz del subárbol, la función devuelve un \_ parámetro de error no válido \_ .

Los nombres de clave no distinguen mayúsculas de minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error. Entre los posibles códigos de error se incluyen los siguientes:

-   Si la subclave especificada no existe, la función devuelve un \_ archivo de error \_ no \_ encontrado.
-   Si la subclave especificada es la clave raíz del subárbol del registro, la función devuelve un parámetro de ERROR \_ no válido \_ .
-   Si la subclave especificada tiene subclaves, la función devuelve la clave de ERROR \_ \_ tiene \_ elementos secundarios.

## <a name="remarks"></a>Observaciones

Si existe la clave del registro especificada, se marca como eliminada. Una clave eliminada no se quita hasta que se cierra el último identificador de la misma.

La clave que se va a eliminar no debe tener subclaves. Para eliminar una clave y todas sus subclaves, utilice la función [**OREnumKey**](orenumkey.md) para enumerar las subclaves y eliminarlas de forma individual.

Solo se puede llamar a la función [**ORCloseKey**](orclosekey.md) en una clave eliminada; se produce un error en todas las demás operaciones de registro sin conexión. Si la clave eliminada se creó explícitamente mediante una llamada a [**ORCreateKey**](orcreatekey.md), se liberarán los recursos asociados a la clave cuando se cierre el último identificador de la clave eliminada.

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

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
