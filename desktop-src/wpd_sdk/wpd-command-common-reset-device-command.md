---
description: El comando de uso \_ \_ común de \_ restablecimiento de dispositivo del comando de WPD \_ restablece el dispositivo. Esto no significa volver a formatear; es equivalente a desactivar y volver a activar el dispositivo.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: Comando WPD_COMMAND_COMMON_RESET_DEVICE (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7ea3fd0088d4997b233670c8ec10bfb16928cb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709252"
---
# <a name="wpd_command_common_reset_device-command"></a>Comando \_ del \_ \_ dispositivo de restablecimiento común de comandos de WPD \_

El comando de uso **\_ común de restablecimiento de \_ \_ \_ dispositivo** del comando de WPD restablece el dispositivo. Esto no significa volver a formatear; es equivalente a desactivar y volver a activar el dispositivo.

## <a name="command-category"></a>Categoría de comando

**\_categoría \_ común de WPD**

## <a name="parameters"></a>Parámetros

Este comando no contiene parámetros.

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

 

 




