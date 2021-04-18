---
description: Recupera las propiedades admitidas por un objeto.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: Comando WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718895"
---
# <a name="wpd_command_object_properties_get_supported-command"></a>\_Propiedades del objeto de comando WPD \_ \_ \_ obtener \_ comando compatible

El comando de **\_ propiedades del objeto de comando WPD \_ \_ \_ Get \_ Supported** recupera las propiedades admitidas por un objeto.

## <a name="command-category"></a>Categoría de comandos

**\_propiedades del \_ objeto de categoría de WPD \_**

## <a name="parameters"></a>Parámetros

El controlador espera el parámetro siguiente.



| Parámetro                                         | VarType        | Descripción                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| **\_identificador de \_ objeto de propiedades del objeto de propiedad WPD \_ \_ \_** | **VT \_ LPWStr** | Obligatorio. IDENTIFICADOR del objeto que contiene las propiedades solicitadas. |



 

## <a name="return-value"></a>Valor devuelto

El controlador debe devolver los resultados siguientes.



| Resultado                                                | VarType         | Descripción                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_claves de \_ propiedad de propiedades del objeto de propiedad WPD \_ \_ \_** | **VT \_ desconocido** | Obligatorio. Una interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que especifica todas las propiedades admitidas.                                                                                                                                                                                                            |
| **\_HRESULT de propiedad \_ común \_ de WPD**                    | **ERROR de VT \_**   | Obligatorio. Un valor **HRESULT** que indica éxito o error general. Los valores de resultado posibles incluyen [códigos de error de dispositivos portátiles de Windows](error-constants.md). Si el autor de la llamada realiza una solicitud no válida, el controlador debe devolver **HRESULT \_ de \_ Win32 (error \_ no \_ admitido)** pero, de lo contrario, no es necesario devolver ningún otro valor de resultado. |
| **\_código de \_ \_ error del controlador común \_ \_ de la propiedad WPD**        | **VT \_ UI4**     | Opcional. Un código de error específico del controlador. Normalmente se usa solo para las pruebas de controladores o si el controlador, el dispositivo y el cliente están diseñados juntos.                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Comandos**](commands.md)
</dt> </dl>

 

 




