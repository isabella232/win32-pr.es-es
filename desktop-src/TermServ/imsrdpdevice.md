---
title: Interfaz IMsRdpDevice
description: Contiene información sobre un objeto de dispositivo.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpDevice Servicios de Escritorio remoto
- Interfaz IMsRdpDevice Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d545bebde1ed2df8a4c67cdf8d32d0a91499ed42076b2c1b31539d96069d3688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033095"
---
# <a name="imsrdpdevice-interface"></a>Interfaz IMsRdpDevice

Contiene información sobre un objeto de dispositivo.

## <a name="members"></a>Miembros

La **interfaz IMsRdpDevice** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpDevice** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpDevice** tiene estas propiedades.



| Propiedad                                                               | Tipo de acceso           | Descripción                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [**DeviceDescription**](imsrdpdevice-devicedescription.md)<br/> | Solo lectura<br/>  | Recupera la descripción del dispositivo que se mostrará al usuario si el nombre para mostrar no está disponible.<br/> |
| [**DeviceInstanceId**](imsrdpdevice-deviceinstanceid.md)<br/>   | Solo lectura<br/>  | Recupera el identificador de instancia de dispositivo del dispositivo.<br/>                                            |
| [**FriendlyName**](imsrdpdevice-friendlyname.md)<br/>           | Solo lectura<br/>  | Recupera el nombre para mostrar del dispositivo.<br/>                                                         |
| [**RedirectionState**](imsrdpdevice-redirectionstate.md)<br/>   | Lectura/escritura<br/> | Indica el estado de redirección del dispositivo.<br/>                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDevice se define como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

