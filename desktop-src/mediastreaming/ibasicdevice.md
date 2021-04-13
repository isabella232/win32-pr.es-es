---
title: Interfaz IBasicDevice
description: Encapsula los métodos y eventos necesarios para modelar un dispositivo DLNA.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- Interfaz IBasicDevice API de streaming de multimedia
- Interfaz IBasicDevice API de streaming de multimedia, descrita
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104421604"
---
# <a name="ibasicdevice-interface"></a>Interfaz IBasicDevice

Encapsula los métodos y eventos necesarios para modelar un dispositivo DLNA.

## <a name="members"></a>Miembros

La interfaz **IBasicDevice** hereda de [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable). **IBasicDevice** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IBasicDevice** tiene estos métodos.



| Método                                                                                 | Descripción                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**agregar \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md)       | Registra un controlador de eventos para el evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .<br/>                |
| [**CanWakeDevices**](ibasicdevice-canwakedevices.md)                                  | Recupera un valor que indica si el dispositivo se puede reactivar.<br/>                                                            |
| [**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))                              | Devuelve un valor de enumeración que indica si el dispositivo está actualmente en línea, fuera de línea o inactivo, pero Reactivable.<br/> |
| [**Descripción**](ibasicdevice-description.md)                                        | Recupera una descripción del dispositivo.<br/>                                                                              |
| [**DiscoveredOnCurrentNetwork**](ibasicdevice-discoveredoncurrentnetwork.md)          | Recupera un valor que indica si el dispositivo está en la red actual.<br/>                                           |
| [**FriendlyName**](ibasicdevice-friendlyname.md)                                      | Recupera el nombre descriptivo del dispositivo.<br/>                                                                               |
| [**Iconos**](ibasicdevice-icons.md)                                                    | Devuelve un vector de interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .<br/>                                                  |
| [**IpAddresses**](ibasicdevice-ipaddresses.md)                                        | Devuelve un vector de direcciones IP.<br/>                                                                                   |
| [**ManufacturerName**](ibasicdevice-manufacturername.md)                              | Recupera el nombre del fabricante del dispositivo.<br/>                                                                           |
| [**ManufacturerUrl**](ibasicdevice-manufacturerurl.md)                                | Recupera la dirección URL del fabricante del dispositivo.<br/>                                                                            |
| [**ModelName**](ibasicdevice-modelname.md)                                            | Recupera el nombre del modelo del dispositivo.<br/>                                                                                  |
| [**ModelNumber**](ibasicdevice-modelnumber.md)                                        | Recupera el número de modelo del dispositivo.<br/>                                                                                |
| [**ModelUrl**](ibasicdevice-modelurl.md)                                              | Recupera la dirección URL del modelo del dispositivo.<br/>                                                                                   |
| [**PhysicalAddresses**](ibasicdevice-physicaladdresses.md)                            | Devuelve un vector de direcciones físicas.<br/>                                                                             |
| [**PresentationUrl**](ibasicdevice-presentationurl.md)                                | Recupera la dirección URL de presentación del dispositivo.<br/>                                                                            |
| [**RemoteStreamingUrls**](ibasicdevice-remotestreamingurls.md)                        | Devuelve un vector de direcciones URL de streaming remoto.<br/>                                                                          |
| [**quitar \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) | Anula el registro de un controlador de eventos para el evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .<br/>              |
| [**SerialNumber**](ibasicdevice-serialnumber.md)                                      | Recupera el número de serie del dispositivo.<br/>                                                                               |
| [**Tipo**](ibasicdevice-type.md)                                                      | Recupera un valor de enumeración que indica el tipo de dispositivo del dispositivo DLNA.<br/>                                       |
| [**UniqueDeviceName**](ibasicdevice-uniquedevicename.md)                              | Recupera el nombre del dispositivo único (UDN).<br/>                                                                    |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

