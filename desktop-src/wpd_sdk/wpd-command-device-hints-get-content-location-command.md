---
description: El comando de las sugerencias de dispositivo de comando de WPD \_ \_ \_ \_ obtener \_ Ubicación de contenido \_ recupera los identificadores de objeto de carpetas que pueden contener un objeto de un tipo especificado.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: Comando WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 22014925455979a8e84b92f1f641cd839df0b9f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708241"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a>Comando de la ubicación de dispositivo de comandos de WPD \_ \_ \_ \_ \_ comando obtener ubicación de contenido \_

El comando de las **sugerencias de dispositivo de comando de WPD \_ \_ \_ \_ obtener \_ \_ Ubicación de contenido** recupera los identificadores de objeto de carpetas que pueden contener un objeto de un tipo especificado. Este comando se proporciona como una manera más rápida para que un cliente detecte dónde un dispositivo almacena objetos específicos que la enumeración de objetos de fuerza bruta.

## <a name="command-category"></a>Categoría de comando

**\_categorías de \_ dispositivos de categoría de WPD \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                   | VarType   | Descripción                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| propiedad de WPD \_ tipo de contenido de \_ sugerencias de dispositivo \_ \_ \_ | VT \_ CLSID | Obligatorio. Tipo de objeto para el que el llamador desea buscar el contenedor. Por ejemplo, para buscar las carpetas de nivel superior usadas para contener imágenes en una cámara digital, el autor de la llamada enviará la imagen de tipo de contenido de WPD \_ \_ \_ . Vea [requisitos para objetos](requirements-for-objects.md) para obtener una lista de tipos de objetos definidos por dispositivos portátiles de Windows. |



 

## <a name="return-value"></a>Valor devuelto

El controlador debe devolver los resultados siguientes.



| Resultado                                               | VarType     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **propiedad de WPD \_ \_ sugerencias de dispositivo \_ \_ ubicaciones de contenido \_** | VT \_ desconocido | Obligatorio. Un [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de tipo VT \_ LPWStr que especifica los identificadores de objeto de carpetas que contienen objetos del tipo indicado por el parámetro de llamada. Si no se encuentra ninguna carpeta, debe ser una lista vacía. Las carpetas indicadas por el resultado pueden contener o no objetos de otros tipos de contenido. Consulte la propiedad tipos de contenido de la [carpeta de WPD \_ \_ \_ \_ permitida](miscellaneous-properties.md) para obtener información sobre las restricciones de carpeta.<br/> |
| **\_HRESULT de propiedad \_ común \_ de WPD**                   | ERROR de VT \_   | Obligatorio. **HRESULT** que indica si el control del comando se ha realizado correctamente o no. Si el autor de la llamada está realizando una solicitud no válida, el controlador debe devolver **HRESULT \_ de \_ Win32 (error \_ no \_ admitido)** y no es necesario devolver ningún otro valor de resultado. Los códigos de error incluyen [códigos de error de dispositivos portátiles de Windows](error-constants.md) o cualquier otro código de error adecuado.                                                                                                                                                                            |
| **\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD**       | VT \_ UI4     | Opcional. Un código de error específico del controlador. Normalmente, esto solo se usa para las pruebas de controladores o si el controlador, el dispositivo y el cliente están diseñados juntos.                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a>Llamar a métodos

Solo se puede llamar directamente a mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

 




