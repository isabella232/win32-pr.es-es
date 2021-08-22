---
description: Define un único método de devolución de llamada.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Interfaz IConnectionRequestCallback (Devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 53e1549767c8577507b3126b3a293dfe4e523612809c144ff24c04dce4ab1ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697423"
---
# <a name="iconnectionrequestcallback-interface"></a>IConnectionRequestCallback (interfaz)

La **interfaz IConnectionRequestCallback** define un único método de devolución de llamada. Una Windows portable Devices (WPD) implementa esta interfaz opcional del Modelo de objetos componentes (COM) para recibir notificaciones sobre las solicitudes completadas y cancelar las solicitudes pendientes. Las solicitudes se envían mediante los métodos [**IPortableDeviceConnector::Conectar**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) [**e IPortableDeviceConnector::D isconnect.**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect)

## <a name="members"></a>Miembros

La **interfaz IConnectionRequestCallback** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IConnectionRequestCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IConnectionRequestCallback** tiene estos métodos.



| Método                                                      | Descripción                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**OnComplete**](iconnectionrequestcallback-oncomplete.md) | Notifica a una aplicación que se ha completado una solicitud programada previamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                                                                             |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



 

