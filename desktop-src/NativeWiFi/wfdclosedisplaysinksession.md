---
description: Limpia el estado de la sesión que se está abriendo o la sesión abierta actualmente.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: Función WFDDisplaySinkCloseSession (Wfdsink. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544238"
---
# <a name="wfddisplaysinkclosesession-function"></a>WFDDisplaySinkCloseSession función)

Limpia el estado de la sesión que se está abriendo o la sesión abierta actualmente.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSessionHandle* \[ de\]
</dt> <dd>

El identificador recibido a través de la invocación de devolución de llamada de notificación del receptor de visualización de WFD más reciente que incluye uno. [**\_ \_ \_ \_**](wfd-display-sink-notification-callback.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

## <a name="remarks"></a>Observaciones

La aplicación puede llamar a esta función para finalizar la sesión de Miracast por cualquier motivo. No es necesario que la aplicación la llame cuando recibe el tipo **DisconnectedNotification** en su devolución de llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 10<br/>                                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2016<br/>                                                             |
| Encabezado<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_devolución de \_ llamada de notificación de receptor de pantalla de \_ WFD \_**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




