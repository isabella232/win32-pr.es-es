---
description: Admite la enumeración de interfaces IPortableDeviceConnector, que representan MTP/Bluetooth dispositivos emparejados con el equipo.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Interfaz IEnumPortableDeviceConnectors (Devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 024d9a813cb20a511c1c23a414625aa78416c530521777ab2c1abaab1c4b4bee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117652759"
---
# <a name="ienumportabledeviceconnectors-interface"></a>Interfaz IEnumPortableDeviceConnectors

La **interfaz IEnumPortableDeviceConnectors** admite la enumeración de interfaces [**IPortableDeviceConnector,**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) que representan los dispositivos MTP/Bluetooth emparejados con el equipo. Tenga en cuenta que esto recuperará todos los dispositivos emparejados previamente, incluidos los dispositivos que están emparejados pero desconectados. Para determinar si un dispositivo sigue conectado, consulte la propiedad **DEVPKEY \_ MTPBTH \_ IsConnected** para ese dispositivo.

## <a name="members"></a>Miembros

La **interfaz IEnumPortableDeviceConnectors** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IEnumPortableDeviceConnectors** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumPortableDeviceConnectors** tiene estos métodos.



| Método                                               | Descripción                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clon**](ienumportabledeviceconnectors-clone.md) | Crea una copia de la interfaz **IEnumPortableDeviceConnectors** actual.<br/>                                                       |
| [**Next**](ienumportabledeviceconnectors-next.md)   | Recupera el siguiente objeto [**IPortableDeviceConnector en**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) la secuencia de enumeración.<br/> |
| [**Restablecer**](ienumportabledeviceconnectors-reset.md) | Restablece la secuencia de enumeración al principio.<br/>                                                                                |
| [**Omitir**](ienumportabledeviceconnectors-skip.md)   | Omite el número especificado de dispositivos en la secuencia de enumeración.<br/>                                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                                                                             |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



 

