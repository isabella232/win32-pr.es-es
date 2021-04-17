---
description: Los comandos de \_ Inicio de captura de imagen del comando WPD \_ \_ \_ \_ inician una captura de imagen continua mediante un objeto funcional de imagen fija. Si se crea un nuevo objeto como resultado de tomar una imagen, el controlador debe enviar el evento de \_ objeto de evento WPD \_ \_ agregado.
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: Comando WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c51c2b4a483588389e9986768a2c617e0fd0dd63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691066"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a>Comando de la \_ \_ captura de \_ imagen del \_ comando de WPD \_

Los comandos de **\_ Inicio de \_ \_ \_ captura \_ de imagen del comando WPD** inician una captura de imagen continua mediante un objeto funcional de imagen fija. Si se crea un nuevo objeto como resultado de tomar una imagen, el controlador debe enviar el evento **de \_ objeto de evento WPD \_ \_ agregado** .

## <a name="command-category"></a>Categoría de comando

**\_captura de \_ \_ imagen \_ de la categoría de WPD**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                              | VarType    | Descripción                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_destino del \_ \_ comando común \_ de la propiedad WPD | VT \_ LPWStr | Obligatorio. El ID. de objeto del objeto funcional de captura de imagen fija en el dispositivo que debe tomar la imagen. Cada objeto funcional de captura de imágenes fijas puede tener una configuración diferente y puede hacer referencia a un hardware diferente en un dispositivo (por ejemplo, una cámara frontal o posterior de un teléfono) y este parámetro indica cuál usar.<br/> |



 

## <a name="return-value"></a>Valor devuelto

El controlador debe devolver los resultados siguientes.



| Resultado                                         | VarType   | Descripción                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_HRESULT de propiedad \_ común \_ de WPD**             | ERROR de VT \_ | Obligatorio. **HRESULT** que indica si se ha realizado correctamente o no el comando. Si el autor de la llamada está realizando una solicitud no válida, el controlador debe devolver **HRESULT \_ de \_ Win32 (error \_ no \_ admitido)** y no es necesario devolver ningún otro valor de resultado. Los códigos de error incluyen [códigos de error de dispositivos portátiles de Windows](error-constants.md) o cualquier otro código de error adecuado. |
| **\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD** | VT \_ UI4   | Opcional. Un código de error específico del controlador. Normalmente, los proveedores de dispositivos usan este valor para mejorar el diagnóstico de errores del dispositivo al usar sus aplicaciones. Las aplicaciones de uso general lo pasarían por alto y solo se basarían en HRESULT de la propiedad de WPD en \_ \_ \_ su lugar.                                                                                                                   |



 

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

 

 




