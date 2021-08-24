---
title: Función WsSetAutoFail (WebServicesDebug.h)
description: Establece el siguiente punto para insertar un error. Se trata de una función DEBUG ONLY.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Servicios web de la función WsSetAutoFail para Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e2ae3ed731edce429aac78700d52d0e7504a5688d1bf35bbb9c64a5d34bc0a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838545"
---
# <a name="wssetautofail-function"></a>Función WsSetAutoFail

Establece el siguiente punto para insertar un error. Se trata de una función DEBUG ONLY.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*count* \[ En\]
</dt> <dd>

Especifica cuántas operaciones antes de que comiencen a producirse errores.

</dd> <dt>

*error* \[ en, opcional\]
</dt> <dd>

Puntero a un objeto [ERROR de WS \_ ](ws-error.md) donde se debe almacenar información adicional sobre el error si se produce un error en la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                       |
| Header<br/>                   | <dl> <dt>WebServicesDebug.h</dt> </dl> |



 

 





