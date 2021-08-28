---
description: El comando WPD \_ COMMAND STORAGE FORMAT da formato a un objeto funcional de almacenamiento en el \_ \_ dispositivo.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: WPD_COMMAND_STORAGE_FORMAT (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 353710bc4167b626b6af001ef535f6d21538a328609aaf05e5e8846415485914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806205"
---
# <a name="wpd_command_storage_format-command"></a>Comando WPD \_ \_ STORAGE FORMAT \_ (Comando)

El **comando WPD \_ COMMAND STORAGE \_ \_ FORMAT** da formato a un objeto funcional de almacenamiento en el dispositivo.

## <a name="command-category"></a>Categoría de comando

**ALMACENAMIENTO DE \_ CATEGORÍA WPD \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                          | VarType    | Descripción                                              |
|------------------------------------|------------|----------------------------------------------------------|
| IDENTIFICADOR DE OBJETO \_ DE ALMACENAMIENTO DE LA PROPIEDAD \_ \_ \_ WPD | VT \_ LPWSTR | Obligatorio. Identificador de objeto del medio de almacenamiento al que se debe dar formato. |



 

## <a name="return-value"></a>Valor devuelto

El controlador debe devolver los resultados siguientes.



| Resultado                                         | VarType   | Descripción                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HRESULT \_ COMÚN DE LA PROPIEDAD \_ \_ WPD**             | \_ERROR DE VT | Obligatorio. HRESULT **que** indica que el comando se ha hecho correctamente o no. Si el autor de la llamada realiza una solicitud no válida, el controlador debe devolver **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** y no es necesario devolver ningún otro valor de resultado. Los códigos de error [Windows códigos de error de dispositivos portátiles](error-constants.md) o cualquier otro código de error adecuado. |
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

 

 




