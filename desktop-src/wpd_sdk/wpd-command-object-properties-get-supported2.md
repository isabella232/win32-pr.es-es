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
ms.openlocfilehash: 5020494658f380abc465a9059544131174edc8c417f69f6322636e6c9d4170d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703985"
---
# <a name="wpd_command_object_properties_get_supported-command"></a>PROPIEDADES DEL \_ OBJETO \_ DE COMANDO WPD GET \_ SUPPORTED \_ \_ Command

El **comando WPD \_ COMMAND OBJECT PROPERTIES GET \_ \_ \_ \_ SUPPORTED** recupera las propiedades admitidas por un objeto .

## <a name="command-category"></a>Categoría de comandos

**PROPIEDADES DE OBJETO \_ DE CATEGORÍA \_ WPD \_**

## <a name="parameters"></a>Parámetros

El controlador espera el parámetro siguiente.



| Parámetro                                         | VarType        | Descripción                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| **WPD \_ PROPERTY \_ OBJECT \_ PROPERTIES \_ OBJECT \_ ID** | **VT \_ LPWSTR** | Obligatorio. Identificador del objeto que contiene las propiedades solicitadas. |



 

## <a name="return-value"></a>Valor devuelto

El controlador debe devolver los resultados siguientes.



| Resultado                                                | VarType         | Descripción                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLAVES DE PROPIEDADES \_ DEL OBJETO \_ DE \_ PROPIEDAD \_ \_ WPD** | **VT \_ UNKNOWN** | Obligatorio. Interfaz [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) que especifica todas las propiedades admitidas.                                                                                                                                                                                                            |
| **HRESULT \_ COMÚN DE LA PROPIEDAD \_ \_ WPD**                    | **\_ERROR DE VT**   | Obligatorio. Valor **HRESULT que** indica el éxito total o el error. Los valores de resultado posibles [incluyen Windows de error de dispositivos portátiles](error-constants.md). Si el autor de la llamada realiza una solicitud no válida, el controlador debe devolver **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** pero, de lo contrario, no es necesario devolver ningún otro valor de resultado. |
| **CÓDIGO DE ERROR \_ COMÚN DEL CONTROLADOR DE LA \_ \_ \_ PROPIEDAD \_ WPD**        | **VT \_ UI4**     | Opcional. Código de error específico del controlador. Esto se suele usar solo para pruebas de controladores, o si el controlador, el dispositivo y el cliente están diseñados conjuntamente.                                                                                                                                                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Comandos**](commands.md)
</dt> </dl>

 

 




