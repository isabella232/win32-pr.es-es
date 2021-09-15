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
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473742"
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

## <a name="remarks"></a>Observaciones

La aplicación puede llamar a esta función para finalizar la Miracast sesión por cualquier motivo. No es necesario que la aplicación la llame cuando recibe el tipo **DisconnectedNotification** en su devolución de llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 10<br/>                                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2016<br/>                                                             |
| Encabezado<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wifidisplay.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DEVOLUCIÓN DE LLAMADA \_ DE NOTIFICACIÓN DEL RECEPTOR DE VISUALIZACIÓN \_ \_ \_ DE WFD**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




