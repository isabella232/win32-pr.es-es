---
description: El controlador de dispositivo usa la interfaz IWpdSerializer para serializar las interfaces IPortableDeviceValues hacia y desde los búferes de datos sin procesar usados para comunicarse con la aplicación. Las aplicaciones no necesitan usar esta interfaz, ya que los datos se serializan y deserializan automáticamente al llamar a IPortableDevice::SendCommand.Para obtener esta interfaz, llame a CoCreateInstance y pase \_ IWpdSerializer de IID.
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Interfaz IWpdSerializer (PortableDeviceTypes.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266847"
---
# <a name="iwpdserializer-interface"></a>IWpdSerializer (interfaz)

El controlador de dispositivo usa la interfaz **IWpdSerializer** para serializar las interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) hacia y desde los búferes de datos sin procesar usados para comunicarse con la aplicación.

Las aplicaciones no necesitan usar esta interfaz, ya que los datos se serializan y deserializan automáticamente al llamar a [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

Para obtener esta interfaz, llame **a CoCreateInstance** y pase **IID \_ IWpdSerializer**.

## <a name="members"></a>Members

La **interfaz IWpdSerializer** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWpdSerializer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWpdSerializer** tiene estos métodos.



| Método                                                                                          | Descripción                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md) | Serializa una interfaz **IPortableDeviceValues** enviada a una matriz de bytes asignada.<br/>                |
| [**GetIPortableDeviceValuesFromBuffer**](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | Deserializa una matriz de bytes en una **interfaz IPortableDeviceValues.**<br/>                                  |
| [**GetSerializedSize**](iwpdserializer-getserializedsize.md)                                   | Calcula el tamaño de búfer necesario para contener una interfaz **IPortableDeviceValues** serializada.<br/> |
| [**WriteIPortableDeviceValuesToBuffer**](iwpdserializer-writeiportabledevicevaluestobuffer.md) | Serializa una interfaz **IPortableDeviceValues** en una matriz de bytes asignada por el autor de la llamada.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaces de controlador**](driver-interfaces.md)
</dt> </dl>

 

