---
description: Define un método de devolución de llamada único.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Interfaz IConnectionRequestCallback (Devpkey. h)
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
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003062"
---
# <a name="iconnectionrequestcallback-interface"></a>Interfaz IConnectionRequestCallback

La interfaz **IConnectionRequestCallback** define un método de devolución de llamada único. Una aplicación de dispositivos portátiles de Windows (WPD) implementa esta interfaz opcional del modelo de objetos componentes (COM) para recibir notificaciones sobre las solicitudes completadas y cancelar las solicitudes pendientes. Las solicitudes se envían mediante los métodos [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) y [**IPortableDeviceConnector::D Ulta**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .

## <a name="members"></a>Miembros

La interfaz **IConnectionRequestCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IConnectionRequestCallback** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IConnectionRequestCallback** tiene estos métodos.



| Método                                                      | Descripción                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**OnComplete (**](iconnectionrequestcallback-oncomplete.md) | Notifica a una aplicación que se ha completado una solicitud programada previamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                                                                             |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                                                                              |
| Encabezado<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Portabledeviceconnectapi. idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



 

