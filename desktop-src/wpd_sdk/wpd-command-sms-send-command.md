---
description: El comando \_ WPD \_ SMS \_ send Command inicia el envío de un mensaje de servicio de mensajes cortos (SMS) por un objeto funcional de SMS.
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: Comando WPD_COMMAND_SMS_SEND (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718695"
---
# <a name="wpd_command_sms_send-command"></a>Comando \_ WPD \_ SMS comando \_ send

El **comando \_ WPD \_ SMS \_ send** Command inicia el envío de un mensaje de servicio de mensajes cortos (SMS) por un objeto funcional de SMS.

## <a name="command-category"></a>Categoría de comando

**\_SMS categoría de WPD \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                              | VarType             | Descripción                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_destino del \_ \_ comando común \_ de la propiedad WPD | VT \_ LPWStr          | Obligatorio. IDENTIFICADOR de objeto del objeto funcional de SMS que debe enviar el mensaje. Distintos objetos funcionales de SMS pueden tener distintas configuraciones.                                                                                     |
| propiedad de WPD \_ \_ destinatario de SMS \_          | VT \_ LPWStr          | Obligatorio. URI del destinatario.                                                                                                                                                                                                  |
| \_tipo de \_ mensaje de SMS de propiedad de WPD \_ \_      | VT \_ UI4             | Obligatorio. Un enumerador de [**\_ \_ tipos de mensajes SMS**](sms-message-types.md) que indica el tipo de mensaje (texto o binario).                                                                                                        |
| \_mensaje de \_ \_ texto SMS de propiedad \_ de WPD      | VT \_ LPWStr          | Opcional. Si **la \_ propiedad de WPD \_ \_ \_ tipo de mensaje de SMS** indica un mensaje de texto, esta es la cadena de mensaje; de lo contrario, este parámetro no se incluye.                                                                                  |
| \_ \_ \_ mensaje binario de SMS de propiedad de WPD \_    | VT \_ Vector \| VT \_ UI1 | Opcional. Si **la \_ propiedad de WPD \_ \_ \_ tipo de mensaje de SMS** indica un mensaje binario, se trata de un puntero a una matriz de bytes; de lo contrario, este parámetro no se incluye. La primera DWORD del valor es la longitud de la matriz, en bytes. |



 

## <a name="return-value"></a>Valor devuelto

El controlador debe devolver los resultados siguientes.



| Resultado                                         | VarType   | Descripción                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_HRESULT de propiedad \_ común \_ de WPD**             | ERROR de VT \_ | Obligatorio. **HRESULT** que indica si se ha realizado correctamente o no el comando. Si el autor de la llamada está realizando una solicitud no válida, el controlador debe devolver **HRESULT \_ de \_ Win32 (error \_ no \_ admitido)** y no es necesario devolver ningún otro valor de resultado. Los códigos de error incluyen [códigos de error de dispositivos portátiles de Windows](error-constants.md) o cualquier otro código de error adecuado. |
| **\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD** | VT \_ UI4   | Opcional. Un código de error específico del controlador. Normalmente, esto solo se usa para las pruebas de controladores o si el controlador, el dispositivo y el cliente están diseñados juntos.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Llamar a métodos

Solo se puede llamar directamente a mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Comandos**](commands.md)
</dt> </dl>

 

 




