---
description: Limpia el estado de la sesión que se va a abrir o la sesión abierta actualmente.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: Función WFDDisplaySinkCloseSession (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7e8169c541535eb2c5adfd0959da47cee4951750687f7d926798534ddc7cbf88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064905"
---
# <a name="wfddisplaysinkclosesession-function"></a>Función WFDDisplaySinkCloseSession

Limpia el estado de la sesión que se va a abrir o la sesión abierta actualmente.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSessionHandle* \[ En\]
</dt> <dd>

Identificador recibido a través de la invocación de devolución de llamada de NOTIFICACIÓN DEL RECEPTOR DE PANTALLA de WFD más reciente que incluía uno. [**\_ \_ \_ \_**](wfd-display-sink-notification-callback.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

## <a name="remarks"></a>Comentarios

La aplicación puede llamar a esta función para finalizar la Miracast sesión por cualquier motivo. No es necesario que la aplicación la llame cuando recibe el tipo **DisconnectedNotification** en su devolución de llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 10<br/>                                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2016<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wifidisplay.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DEVOLUCIÓN DE LLAMADA \_ DE NOTIFICACIÓN DEL RECEPTOR DE VISUALIZACIÓN \_ \_ \_ DE WFD**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




