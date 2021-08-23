---
description: Elimina una subclave y sus valores de un subárbol del Registro sin conexión.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Función ORDeleteKey (Offreg.h)
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
ms.openlocfilehash: 9f3be934eca97d88f4dfeb1b1576d9fcd06f5681351a2e85d8ae7f6ba31e8860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571935"
---
# <a name="ordeletekey-function"></a>Función ORDeleteKey

Elimina una subclave y sus valores de un subárbol del Registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión. La función [**ORCreateKey**](orcreatekey.md) o [**OROpenKey**](oropenkey.md) devuelve este identificador.

</dd> <dt>

*lpSubKey* \[ en, opcional\]
</dt> <dd>

Nombre de la clave que se va a eliminar. Debe ser una subclave de la clave que *Handle* identifica, pero no puede tener subclaves.

Si la subclave no existe, la función devuelve ERROR \_ NOT \_ FOUND.

Si este parámetro es **NULL,** la función elimina la clave especificada por el *parámetro Handle.* Si la clave especificada por el parámetro *Handle* es la clave raíz del subárbol, la función devuelve ERROR \_ INVALID \_ PARAMETER.

Los nombres de clave no distinguen mayúsculas de minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error. Entre los posibles códigos de error se incluyen los siguientes:

-   Si la subclave especificada no existe, la función devuelve ERROR \_ FILE \_ NOT \_ FOUND.
-   Si la subclave especificada es la clave raíz del subárbol del Registro, la función devuelve ERROR \_ INVALID \_ PARAMETER.
-   Si la subclave especificada tiene subclaves, la función devuelve ERROR \_ KEY \_ HAS \_ CHILDREN.

## <a name="remarks"></a>Comentarios

Si existe la clave del Registro especificada, se marca como eliminada. Una clave eliminada no se quita hasta que se cierra el último identificador para ella.

La clave que se va a eliminar no debe tener subclaves. Para eliminar una clave y todas sus subclaves, use la función [**OREnumKey**](orenumkey.md) para enumerar las subclaves y eliminarlas individualmente.

Solo se [**puede llamar a la función ORCloseKey**](orclosekey.md) en una clave eliminada. todas las demás operaciones del Registro sin conexión producirán un error. Si la clave eliminada se creó explícitamente mediante una llamada a [**ORCreateKey**](orcreatekey.md), los recursos asociados a la clave se liberan cuando se cierra el último identificador de la clave eliminada.

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

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
