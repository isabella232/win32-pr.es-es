---
description: Realiza la inicialización necesaria para permitir que la aplicación que realiza la llamada se convierta en un receptor Miracast pantalla.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: Función WFDDisplaySinkStart (Wfdsink.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473739"
---
# <a name="wfddisplaysinkstart-function"></a>Función WFDDisplaySinkStart

Realiza la inicialización necesaria para permitir que la aplicación que realiza la llamada se convierta en un receptor Miracast pantalla. La aplicación debe llamar a esto una vez en el inicio.

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

*uDeviceCategory* \[ En\]
</dt> <dd>

Categoría del dispositivo.

</dd> <dt>

*uSubCategory* \[ En\]
</dt> <dd>

Subcategoría del dispositivo.

</dd> <dt>

*pCallbackContext* \[ en, opcional\]
</dt> <dd>

Puntero de contexto opcional que se pasa a la función de devolución de llamada especificada en el *parámetro pfnCallback.*

</dd> <dt>

*pfnCallback* \[ En\]
</dt> <dd>

Puntero a la función de devolución de llamada a la que se llamará cada vez que haya una notificación para la aplicación. Las notificaciones que se pueden enviar se describen en [**WFD \_ DISPLAY SINK \_ NOTIFICATION \_ \_ CALLBACK**](wfd-display-sink-notification-callback.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de retorno.



| Código devuelto                                                                                          | Descripción                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**ERROR \_ NO \_ ADMITIDO**</dt> </dl> | El receptor de pantalla no se admite en este hardware.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta función realiza las siguientes tareas:

-   Hace que el equipo sea reconocible
-   Establece la información del dispositivo P2P para reflejar la categoría y la subcategoría especificadas.
-   Establece las Miracast en todos los Wi-Fi marcos directos con el tipo de dispositivo como receptor
-   Registra la devolución de llamada especificada que se invocará siempre que haya una conexión entrante.

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

 

 




