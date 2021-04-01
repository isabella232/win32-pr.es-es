---
title: Interfaces de streaming multimedia
description: La API de streaming de multimedia proporciona las siguientes interfaces.
ms.assetid: 1E25B452-D23C-4A1D-BC39-A5B719DF2C5D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6cdb1893af3170ae9ec5989498a007230992361
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103995822"
---
# <a name="media-streaming-interfaces"></a>Interfaces de streaming multimedia

La [API de streaming de multimedia](media-streaming-api-portal.md) proporciona las siguientes interfaces.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                 | Descripción                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice)<br/>                           | Representa un [**IBasicDevice**](ibasicdevice.md) activo que está asociado a un dispositivo UPnP. <br/>                                                                                                                                          |
| [**IActiveBasicDeviceStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics)<br/>             | Proporciona métodos estáticos para crear objetos [**IActiveBasicDevice**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice) . <br/>                                                                                                                                            |
| [**IBasicDevice**](ibasicdevice.md)<br/>                                       | Encapsula los métodos y eventos necesarios para modelar un dispositivo DLNA.<br/>                                                                                                                                                                         |
| [**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)<br/>                             | Encapsula los métodos y eventos necesarios para recuperar una lista de representadores de medios digitales (DMRs) y/o servidores multimedia digitales (DMSs) almacenados en memoria caché, o para buscar de forma asincrónica los DMRs y/o DMSs que están actualmente en la red.<br/>              |
| [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)<br/>                                         | Encapsula los métodos necesarios para proporcionar información sobre el icono de un dispositivo DLNA.<br/>                                                                                                                                                    |
| [**IDevicePair**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicepair)<br/>                                         | Representa un par de objetos [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) que se componen de un representador y un servidor.<br/>                                                                                                                 |
| [**IMediaRenderer**](imediarenderer.md)<br/>                                   | Encapsula los métodos y eventos necesarios para representar un dispositivo de representador de medios digitales DLNA (DMR).<br/>                                                                                                                                        |
| [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)<br/> | Encapsula los métodos necesarios para proporcionar información sobre los métodos que se pueden invocar actualmente en el DMR.<br/>                                                                                                                             |
| [**IMediaRendererFactory**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)<br/>                     | Encapsula los métodos necesarios para crear de forma asincrónica una nueva instancia de un objeto que implementa la interfaz [**IMediaRenderer**](imediarenderer.md) .<br/>                                                                               |
| [**IStreamSelectorStatics**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-istreamselectorstatics)<br/>                   | Encapsula los métodos necesarios para seleccionar un flujo de forma asincrónica.<br/>                                                                                                                                                                         |
| [**ITransportParameters**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)<br/>                       | Encapsula los métodos necesarios para proporcionar información sobre la configuración actual relacionada con el transporte de DMR. Esta configuración incluye el estado de transporte actual e información sobre los métodos que se pueden invocar actualmente en el DMR.<br/> |



 

 

