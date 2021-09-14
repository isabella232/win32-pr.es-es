---
title: Interfaces de streaming multimedia
description: Media Streaming API proporciona las interfaces siguientes.
ms.assetid: 1E25B452-D23C-4A1D-BC39-A5B719DF2C5D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6cdb1893af3170ae9ec5989498a007230992361
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248493"
---
# <a name="media-streaming-interfaces"></a>Interfaces de streaming multimedia

Media [Streaming API proporciona](media-streaming-api-portal.md) las interfaces siguientes.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                 | Descripción                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice)<br/>                           | Representa un [**IBasicDevice activo**](ibasicdevice.md) asociado a un dispositivo UPnP. <br/>                                                                                                                                          |
| [**IActiveBasicDeviceStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics)<br/>             | Proporciona métodos estáticos para crear [**objetos IActiveBasicDevice.**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice) <br/>                                                                                                                                            |
| [**IBasicDevice**](ibasicdevice.md)<br/>                                       | Encapsula los métodos y eventos necesarios para modelar un dispositivo DLNA.<br/>                                                                                                                                                                         |
| [**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)<br/>                             | Encapsula los métodos y eventos necesarios para recuperar una lista de representadores multimedia digitales (DMR) y/o servidores multimedia digitales (DMS) almacenados en caché, o para buscar asincrónicamente las DMR o DMS que están actualmente en la red.<br/>              |
| [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)<br/>                                         | Encapsula los métodos necesarios para proporcionar información sobre el icono de un dispositivo DLNA.<br/>                                                                                                                                                    |
| [**IDevicePair**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicepair)<br/>                                         | Representa un par de [**objetos ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) que consta de un representador y un servidor.<br/>                                                                                                                 |
| [**IMediaRenderer**](imediarenderer.md)<br/>                                   | Encapsula los métodos y eventos necesarios para representar un dispositivo DLNA Digital Media Renderer (DMR).<br/>                                                                                                                                        |
| [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)<br/> | Encapsula los métodos necesarios para proporcionar información sobre qué métodos se pueden invocar actualmente en la DMR.<br/>                                                                                                                             |
| [**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)<br/>                     | Encapsula los métodos necesarios para crear de forma asincrónica una nueva instancia de un objeto que implementa la [**interfaz IMediaRenderer.**](imediarenderer.md)<br/>                                                                               |
| [**IStreamSelectorStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-istreamselectorstatics)<br/>                   | Encapsula los métodos necesarios para seleccionar de forma asincrónica una secuencia.<br/>                                                                                                                                                                         |
| [**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)<br/>                       | Encapsula los métodos necesarios para proporcionar información sobre la configuración actual relacionada con el transporte de la DMR. Esta configuración incluye el estado de transporte actual e información sobre qué métodos se pueden invocar actualmente en la DMR.<br/> |



 

 

