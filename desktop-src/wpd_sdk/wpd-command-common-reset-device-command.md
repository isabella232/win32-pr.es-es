---
description: El comando WPD \_ COMMAND COMMON RESET DEVICE restablece el \_ \_ \_ dispositivo. Esto no significa volver a formatear; equivale a apagar y volver a activar el dispositivo.
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: WPD_COMMAND_COMMON_RESET_DEVICE (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467045"
---
# <a name="wpd_command_common_reset_device-command"></a>COMANDO WPD \_ COMANDO COMMON RESET DEVICE \_ \_ \_ Command

El **comando WPD \_ COMMAND COMMON \_ RESET \_ \_ DEVICE** restablece el dispositivo. Esto no significa volver a formatear; equivale a apagar y volver a activar el dispositivo.

## <a name="command-category"></a>Categoría de comando

**CATEGORÍA WPD \_ \_ COMÚN**

## <a name="parameters"></a>Parámetros

Este comando no contiene parámetros.

## <a name="return-value"></a>Valor devuelto

El controlador debe devolver los resultados siguientes.



| Resultado                                         | VarType   | Descripción                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HRESULT \_ COMÚN DE LA PROPIEDAD \_ \_ WPD**             | \_ERROR DE VT | Necesario. HRESULT **que** indica que el comando se ha hecho correctamente o no. Si el autor de la llamada realiza una solicitud no válida, el controlador debe devolver **HRESULT \_ FROM \_ WIN32 (ERROR \_ NO \_ COMPATIBLE)** y no es necesario devolver ningún otro valor de resultado. Los códigos de error [Windows códigos de error de dispositivos portátiles](error-constants.md) o cualquier otro código de error adecuado. |
| **CÓDIGO DE ERROR \_ COMÚN DEL CONTROLADOR DE LA \_ \_ \_ PROPIEDAD \_ WPD** | VT \_ UI4   | Opcional. Código de error específico del controlador. Normalmente, esto solo se usa para las pruebas de controladores, o si el controlador, el dispositivo y el cliente están diseñados conjuntamente.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Llamar a métodos

Solo se puede llamar directamente mediante [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Comandos**](commands.md)
</dt> </dl>

 

 




