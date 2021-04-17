---
title: MB_GetString función (User. h)
description: Devuelve cadenas para los botones de cuadro de mensaje estándar.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- MB_GetString cuadros de diálogo de función
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafd33f268f2ef1ef87755b79aba6d5d0aa77bb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700102"
---
# <a name="mb_getstring-function"></a>MB \_ GetString (función)

Devuelve cadenas para los botones de cuadro de mensaje estándar.

## <a name="syntax"></a>Sintaxis


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wBtn* 
</dt> <dd>

Identificador de la cadena que se va a devolver. Se identifican mediante los valores de identificador de comando del cuadro de diálogo enumerados en Winuser. h.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La cadena o NULL si no se encuentra.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>User. h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>User32. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>User32.dll</dt> </dl> |



 

 





