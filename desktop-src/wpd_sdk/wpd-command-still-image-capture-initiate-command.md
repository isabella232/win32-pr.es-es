---
description: El comando WPD COMMAND STILL IMAGE CAPTURE INITIATE inicia una captura de imagen fija \_ mediante un objeto funcional de imagen \_ \_ \_ \_ fija. Si se crea un nuevo objeto como resultado de tomar una imagen, el controlador debe enviar el evento \_ WPD EVENT \_ OBJECT \_ ADDED.
ms.assetid: 2968b96e-c9d8-42a7-a32a-dea5fdf064b5
title: WPD_COMMAND_STILL_IMAGE_CAPTURE_INITIATE (PortableDevice.h)
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
ms.openlocfilehash: 5c5490a5af583753f504decacaccf4b4373890fdb7f0e5b099389df29cdc0571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806285"
---
# <a name="wpd_command_still_image_capture_initiate-command"></a>Comando WPD \_ COMANDO STILL IMAGE CAPTURE \_ \_ \_ \_ INITIATE

El **comando WPD \_ COMMAND STILL IMAGE CAPTURE \_ \_ \_ \_ INITIATE** inicia una captura de imagen fija mediante un objeto funcional de imagen fija. Si se crea un nuevo objeto como resultado de tomar una imagen, el controlador debe enviar el evento **\_ WPD EVENT \_ OBJECT \_ ADDED.**

## <a name="command-category"></a>Categoría de comando

**CAPTURA DE IMÁGENES \_ DE LA CATEGORÍA \_ WPD \_ \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                              | VarType    | Descripción                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DESTINO DE COMANDO \_ COMÚN DE LA \_ PROPIEDAD WPD \_ \_ | VT \_ LPWSTR | Obligatorio. El identificador de objeto del objeto funcional de captura de imagen fija en el dispositivo que debe tomar la imagen. Cada objeto funcional de captura de imágenes fijas puede tener una configuración diferente y puede hacer referencia a hardware diferente en un dispositivo (por ejemplo, una cámara frontal o posterior de un teléfono) y este parámetro indica cuál usar.<br/> |



 

## <a name="return-value"></a>Valor devuelto

El controlador debe devolver los resultados siguientes.



| Resultado                                         | VarType   | Descripción                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HRESULT \_ COMÚN DE LA PROPIEDAD \_ \_ WPD**             | \_ERROR DE VT | Obligatorio. HRESULT **que** indica que el comando se ha hecho correctamente o no. Si el autor de la llamada realiza una solicitud no válida, el controlador debe devolver **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** y no es necesario devolver ningún otro valor de resultado. Los códigos de error [Windows códigos de error de dispositivos portátiles](error-constants.md) o cualquier otro código de error adecuado. |
| **CÓDIGO DE ERROR \_ COMÚN DEL CONTROLADOR DE LA \_ \_ \_ PROPIEDAD \_ WPD** | VT \_ UI4   | Opcional. Código de error específico del controlador. Este valor lo usan normalmente los proveedores de dispositivos para mejorar el diagnóstico de errores de dispositivos al usar sus aplicaciones. Las aplicaciones de uso general lo ignorarían y se basaban únicamente en WPD \_ PROPERTY \_ COMMON \_ HRESULT en su lugar.                                                                                                                   |



 

## <a name="calling-methods"></a>Llamar a métodos

Solo se puede llamar directamente mediante [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Comandos**](commands.md)
</dt> </dl>

 

 




