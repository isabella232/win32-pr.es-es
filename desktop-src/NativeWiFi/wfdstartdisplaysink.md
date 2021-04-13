---
description: Realiza la inicialización necesaria para permitir que la aplicación que realiza la llamada se convierta en un receptor de pantalla Miracast.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: Función WFDDisplaySinkStart (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544235"
---
# <a name="wfddisplaysinkstart-function"></a>WFDDisplaySinkStart función)

Realiza la inicialización necesaria para permitir que la aplicación que realiza la llamada se convierta en un receptor de pantalla Miracast. La aplicación debe llamarla una vez al inicio.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uDeviceCategory* \[ de\]
</dt> <dd>

La categoría de dispositivos.

</dd> <dt>

*uSubCategory* \[ de\]
</dt> <dd>

Subcategoría del dispositivo.

</dd> <dt>

*pCallbackContext* \[ en, opcional\]
</dt> <dd>

Un puntero de contexto opcional que se pasa a la función de devolución de llamada especificada en el parámetro *pfnCallback* .

</dd> <dt>

*pfnCallback* \[ de\]
</dt> <dd>

Un puntero a la función de devolución de llamada a la que se llamará siempre que haya una notificación para la aplicación. Las notificaciones que se pueden enviar se describen en la [**devolución de llamada de notificación de receptor de visualización de WFD \_ \_ \_ \_**](wfd-display-sink-notification-callback.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de retorno.



| Código devuelto                                                                                          | Descripción                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**ERROR \_ no \_ admitido**</dt> </dl> | El receptor de pantalla no es compatible con este hardware.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta función realiza las siguientes tareas:

-   Hace que el equipo sea reconocible
-   Establece la información del dispositivo P2P para reflejar la categoría y la subcategoría especificada.
-   Establece las s de Miracast en todas Wi-Fi tramas directas con el tipo de dispositivo como receptor
-   Registra la devolución de llamada especificada que se va a invocar siempre que haya una conexión entrante.

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

 

 




