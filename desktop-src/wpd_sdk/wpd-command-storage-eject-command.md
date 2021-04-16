---
description: El \_ comando de expulsión de almacenamiento de comandos de WPD \_ \_ expulsa un medio de almacenamiento que el equipo puede retirar de forma remota.
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: Comando WPD_COMMAND_STORAGE_EJECT (PortableDevice. h)
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
ms.openlocfilehash: 3eab2c6296b957b8edf1d65f21264cb93144aeb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649969"
---
# <a name="wpd_command_storage_eject-command"></a>\_Comando de \_ retiro de almacenamiento de comandos de WPD \_

El comando de **\_ \_ \_ expulsión de almacenamiento de comandos de WPD** expulsa un medio de almacenamiento que el equipo puede retirar de forma remota.

## <a name="command-category"></a>Categoría de comando

**\_almacenamiento de categorías de WPD \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                          | VarType    | Descripción                                             |
|------------------------------------|------------|---------------------------------------------------------|
| \_identificador de \_ objeto de almacenamiento de propiedades de WPD \_ \_ | VT \_ LPWStr | Obligatorio. IDENTIFICADOR de objeto del objeto de almacenamiento que se va a expulsar. |



 

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

 

 




