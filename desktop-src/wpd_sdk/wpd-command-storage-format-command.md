---
description: El comando de formato de almacenamiento de comandos de WPD \_ \_ \_ da formato a un objeto funcional de almacenamiento en el dispositivo.
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: Comando WPD_COMMAND_STORAGE_FORMAT (PortableDevice. h)
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
ms.openlocfilehash: 763323a8c2a66319ab84636a5d7b2d46a6edb37d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649968"
---
# <a name="wpd_command_storage_format-command"></a>\_Comando de \_ formato de almacenamiento de comandos de WPD \_

El comando de formato de almacenamiento de comandos de WPD da formato a un objeto funcional de almacenamiento en el dispositivo. **\_ \_ \_**

## <a name="command-category"></a>Categoría de comando

**\_almacenamiento de categorías de WPD \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                          | VarType    | Descripción                                              |
|------------------------------------|------------|----------------------------------------------------------|
| \_identificador de \_ objeto de almacenamiento de propiedades de WPD \_ \_ | VT \_ LPWStr | Obligatorio. IDENTIFICADOR de objeto del medio de almacenamiento al que se va a dar formato. |



 

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

 

 




