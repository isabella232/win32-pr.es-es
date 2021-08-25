---
description: El comando WPD COMMAND STORAGE EYE expulsa un medio de almacenamiento que el equipo puede expulsar \_ \_ de forma \_ remota.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: WPD_COMMAND_STORAGE_EJECT (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2a35b376ed9688217edfde03c76aed962d3e5fb74dc3d8bb7cc927ef1f621c9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839015"
---
# <a name="wpd_command_storage_eject-command"></a>Comando WPD \_ STORAGE DEL COMANDO DE \_ \_ EXPULSIÓN

El **comando WPD \_ COMMAND STORAGE \_ \_ EJECT** expulsa un medio de almacenamiento que el equipo puede expulsar de forma remota.

## <a name="command-category"></a>Categoría de comando

**ALMACENAMIENTO DE \_ CATEGORÍA WPD \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                          | VarType    | Descripción                                             |
|------------------------------------|------------|---------------------------------------------------------|
| IDENTIFICADOR DE OBJETO \_ DE ALMACENAMIENTO DE LA PROPIEDAD \_ \_ \_ WPD | VT \_ LPWSTR | Obligatorio. Identificador de objeto del objeto de almacenamiento que se expulsará. |



 

## <a name="return-value"></a>Valor devuelto

El controlador debe devolver los resultados siguientes.



| Resultado                                         | VarType   | Descripción                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HRESULT \_ COMÚN DE LA PROPIEDAD \_ \_ WPD**             | \_ERROR DE VT | Obligatorio. HRESULT **que** indica que el comando se ha hecho correctamente o no. Si el autor de la llamada realiza una solicitud no válida, el controlador debe devolver **HRESULT \_ FROM \_ WIN32 (ERROR \_ NO \_ COMPATIBLE)** y no es necesario devolver ningún otro valor de resultado. Los códigos de error [Windows códigos de error de dispositivos portátiles](error-constants.md) o cualquier otro código de error adecuado. |
| **CÓDIGO DE ERROR \_ COMÚN DEL CONTROLADOR DE LA \_ \_ \_ PROPIEDAD \_ WPD** | VT \_ UI4   | Opcional. Código de error específico del controlador. Normalmente, esto solo se usa para pruebas de controladores, o si el controlador, el dispositivo y el cliente están diseñados conjuntamente.                                                                                                                                                                                                                                |



 

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

 

 




