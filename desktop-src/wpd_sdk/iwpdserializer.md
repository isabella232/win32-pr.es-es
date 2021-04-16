---
description: 'El controlador de dispositivo usa la interfaz IWpdSerializer para serializar las interfaces IPortableDeviceValues en los búferes de datos sin procesar que se usan para comunicarse con la aplicación. Las aplicaciones no necesitan usar esta interfaz, porque los datos se serializan y deserializan automáticamente al llamar a IPortableDevice:: SendCommand. para obtener esta interfaz, llame a CoCreateInstance y pase el IID \_ IWpdSerializer.'
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Interfaz IWpdSerializer (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: dde4bfeea596ccc2691323d484f5583d55ade621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671278"
---
# <a name="iwpdserializer-interface"></a>Interfaz IWpdSerializer

El controlador de dispositivo usa la interfaz **IWpdSerializer** para serializar las interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) en los búferes de datos sin procesar que se usan para comunicarse con la aplicación.

Las aplicaciones no necesitan usar esta interfaz, porque los datos se serializan y deserializan automáticamente al llamar a [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

Para obtener esta interfaz, llame a **CoCreateInstance** y pase el **IID \_ IWpdSerializer**.

## <a name="members"></a>Miembros

La interfaz **IWpdSerializer** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWpdSerializer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWpdSerializer** tiene estos métodos.



| Método                                                                                          | Descripción                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md) | Serializa una interfaz **IPortableDeviceValues** enviada a una matriz de bytes asignada.<br/>                |
| [**GetIPortableDeviceValuesFromBuffer**](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | Deserializa una matriz de bytes en una interfaz **IPortableDeviceValues** .<br/>                                  |
| [**GetSerializedSize**](iwpdserializer-getserializedsize.md)                                   | Calcula el tamaño del búfer necesario para contener una interfaz **IPortableDeviceValues** serializada.<br/> |
| [**WriteIPortableDeviceValuesToBuffer**](iwpdserializer-writeiportabledevicevaluestobuffer.md) | Serializa una interfaz **IPortableDeviceValues** en una matriz de bytes asignada por el llamador.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces de controlador**](driver-interfaces.md)
</dt> </dl>

 

