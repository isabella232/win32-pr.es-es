---
title: Función WsSetAutoFail (WebServicesDebug. h)
description: Establece el siguiente punto para insertar un error. Se trata de una función de solo depuración.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Servicios Web de la función WsSetAutoFail para Windows
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
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534924"
---
# <a name="wssetautofail-function"></a>WsSetAutoFail función)

Establece el siguiente punto para insertar un error. Se trata de una función de solo depuración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*recuento* \[ de\]
</dt> <dd>

Especifica cuántas operaciones antes de que se produzcan errores.

</dd> <dt>

*error* \[ de en, opcional\]
</dt> <dd>

Un puntero a un objeto de [ \_ error de WS](ws-error.md) en el que se debe almacenar información adicional sobre el error si se produce un error en la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>WebServicesDebug. h</dt> </dl> |



 

 





