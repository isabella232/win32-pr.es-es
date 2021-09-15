---
description: Recupera las propiedades admitidas por un objeto .
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570128"
---
# <a name="wpd_command_object_properties_get_supported-command"></a>PROPIEDADES DEL \_ OBJETO \_ DE COMANDO WPD GET \_ SUPPORTED \_ \_ COMMAND

El **comando WPD \_ COMMAND OBJECT PROPERTIES GET \_ \_ \_ \_ SUPPORTED** recupera las propiedades admitidas por un objeto .

## <a name="command-category"></a>Categoría de comandos

**PROPIEDADES DE OBJETO \_ DE CATEGORÍA \_ \_ WPD**

## <a name="parameters"></a>Parámetros

El controlador espera el parámetro siguiente.



| Parámetro                                         | VarType        | Descripción                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| **IDENTIFICADOR DE OBJETO \_ DE PROPIEDADES DE OBJETO DE PROPIEDAD \_ \_ \_ \_ WPD** | **VT \_ LPWSTR** | Necesario. Identificador del objeto que contiene las propiedades solicitadas. |



 

## <a name="return-value"></a>Valor devuelto

El controlador debe devolver los resultados siguientes.



| Resultado                                                | VarType         | Descripción                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLAVES DE PROPIEDAD \_ DE PROPIEDADES DEL OBJETO DE PROPIEDAD \_ \_ \_ \_ WPD** | **VT \_ UNKNOWN** | Necesario. Interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que especifica todas las propiedades admitidas.                                                                                                                                                                                                            |
| **PROPIEDAD WPD \_ \_ COMMON \_ HRESULT**                    | **\_ERROR DE VT**   | Necesario. Valor **HRESULT que** indica el éxito o error general. Los valores de resultado posibles [incluyen Windows de error de dispositivos portátiles](error-constants.md). Si el autor de la llamada realiza una solicitud no válida, el controlador debe devolver **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** pero, de lo contrario, no es necesario devolver ningún otro valor de resultado. |
| **CÓDIGO DE ERROR \_ COMÚN DEL CONTROLADOR DE LA PROPIEDAD \_ \_ \_ \_ WPD**        | **VT \_ UI4**     | Opcional. Código de error específico del controlador. Esto se usa normalmente solo para pruebas de controladores, o si el controlador, el dispositivo y el cliente están diseñados juntos.                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Comandos**](commands.md)
</dt> </dl>

 

 




