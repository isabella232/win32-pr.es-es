---
description: Admite la enumeración de interfaces de IPortableDeviceConnector, que representan dispositivos MTP/Bluetooth que se emparejaron con el equipo.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Interfaz IEnumPortableDeviceConnectors (Devpkey. h)
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
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276877"
---
# <a name="ienumportabledeviceconnectors-interface"></a>Interfaz IEnumPortableDeviceConnectors

La interfaz **IEnumPortableDeviceConnectors** admite la enumeración de interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , que representan dispositivos MTP/Bluetooth que se emparejaron con el equipo. Tenga en cuenta que esto recuperará todos los dispositivos emparejados previamente, incluidos los dispositivos emparejados pero desconectados. Para determinar si un dispositivo sigue conectado, consulte la propiedad **DEVPKEY \_ MTPBTH \_ IsConnected** para ese dispositivo.

## <a name="members"></a>Miembros

La interfaz **IEnumPortableDeviceConnectors** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumPortableDeviceConnectors** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IEnumPortableDeviceConnectors** tiene estos métodos.



| Método                                               | Descripción                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clonar**](ienumportabledeviceconnectors-clone.md) | Crea una copia de la interfaz **IEnumPortableDeviceConnectors** actual.<br/>                                                       |
| [**Next**](ienumportabledeviceconnectors-next.md)   | Recupera los siguientes objetos [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) en la secuencia de enumeración.<br/> |
| [**Reset**](ienumportabledeviceconnectors-reset.md) | Restablece la secuencia de enumeración al principio.<br/>                                                                                |
| [**Omitir**](ienumportabledeviceconnectors-skip.md)   | Omite el número especificado de dispositivos en la secuencia de enumeración.<br/>                                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                                                                             |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                              |
| Encabezado<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portabledeviceconnectapi. idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



 

