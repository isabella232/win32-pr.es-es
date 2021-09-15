---
description: El comando WPD COMMAND DEVICE HINTS GET CONTENT LOCATION recupera los \_ \_ \_ \_ \_ iDs de objeto de las \_ carpetas que pueden contener un objeto de un tipo especificado.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466647"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a>Comando WPD \_ \_ COMMAND DEVICE \_ HINTS GET CONTENT LOCATION \_ \_ (COMANDO GET CONTENT \_ LOCATION)

El **comando WPD \_ COMMAND DEVICE \_ \_ HINTS GET CONTENT \_ \_ \_ LOCATION** recupera los iDs de objeto de las carpetas que pueden contener un objeto de un tipo especificado. Este comando se proporciona como una manera más rápida de que un cliente detecte dónde almacena un dispositivo objetos específicos que mediante la enumeración de objetos bruta.

## <a name="command-category"></a>Categoría de comando

**SUGERENCIAS DE \_ DISPOSITIVO \_ DE CATEGORÍA WPD \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                   | VarType   | Descripción                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPO DE CONTENIDO \_ DE \_ \_ SUGERENCIAS DE DISPOSITIVO DE \_ PROPIEDAD \_ WPD | VT \_ CLSID | Necesario. Tipo de objeto para el que el autor de la llamada desea encontrar el contenedor. Por ejemplo, para buscar las carpetas de nivel superior que se usan para contener imágenes en una cámara digital, el autor de la llamada enviaría WPD \_ CONTENT \_ TYPE \_ IMAGE. Vea [Requisitos para objetos para](requirements-for-objects.md) obtener una lista de tipos de objetos definidos por Windows dispositivos portátiles. |



 

## <a name="return-value"></a>Valor devuelto

El controlador debe devolver los resultados siguientes.



| Resultado                                               | VarType     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **UBICACIONES DE CONTENIDO \_ DE \_ \_ SUGERENCIAS DE DISPOSITIVO DE \_ PROPIEDAD WPD \_** | VT \_ UNKNOWN | Necesario. [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de tipo VT LPWSTR valores que especifican los id. de objeto de las carpetas que contienen objetos del tipo indicado por el parámetro \_ de llamada. Si no se encuentra ninguna carpeta, debe ser una lista vacía. Las carpetas indicadas por el resultado pueden o no contener objetos de otros tipos de contenido. Consulte la propiedad [WPD \_ FOLDER CONTENT TYPES ALLOWED \_ \_ \_ para](miscellaneous-properties.md) obtener información sobre las restricciones de carpetas.<br/> |
| **HRESULT \_ COMÚN DE LA PROPIEDAD \_ \_ WPD**                   | \_ERROR DE VT   | Necesario. HRESULT **que** indica que el control del comando se ha hecho correctamente o no. Si el autor de la llamada realiza una solicitud no válida, el controlador debe devolver **HRESULT \_ FROM \_ WIN32 (ERROR \_ NO \_ COMPATIBLE)** y no es necesario devolver ningún otro valor de resultado. Los códigos de error [Windows códigos de error de dispositivos portátiles](error-constants.md) o cualquier otro código de error adecuado.                                                                                                                                                                            |
| **CÓDIGO DE ERROR \_ COMÚN DEL CONTROLADOR DE LA \_ \_ \_ PROPIEDAD \_ WPD**       | VT \_ UI4     | Opcional. Código de error específico del controlador. Normalmente, esto solo se usa para las pruebas de controladores, o si el controlador, el dispositivo y el cliente están diseñados conjuntamente.                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a>Llamar a métodos

Solo se puede llamar directamente mediante [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

 




