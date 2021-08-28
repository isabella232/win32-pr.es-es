---
title: MB_GetString (User.h)
description: Devuelve cadenas para los botones de cuadro de mensaje estándar.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- MB_GetString cuadros de diálogo de la función
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
ms.openlocfilehash: 9bdd984a2f65ab8c2eed8a77fffa56af1d94633c828196428a674c9eee78c3ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985365"
---
# <a name="mb_getstring-function"></a>Función \_ GetString de MB

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

Identificador de la cadena que se devuelve. Estos se identifican mediante los valores de Identificador de comando del cuadro de diálogo enumerados en winuser.h.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena o NULL si no se encuentra.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>User.h</dt> </dl>     |
| Biblioteca<br/> | <dl> <dt>User32.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>User32.dll</dt> </dl> |



 

 





