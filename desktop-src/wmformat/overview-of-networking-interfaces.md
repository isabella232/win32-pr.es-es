---
title: Información general de las interfaces de red
description: Información general de las interfaces de red
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- SDK de Windows Media Format, interfaces de red
- SDK de Windows Media Format, interfaces
- Advanced Systems Format (ASF), interfaces de red
- ASF (formato de sistemas avanzados), interfaces de red
- Advanced Systems Format (ASF), lista de interfaces para características de red
- ASF (formato de sistemas avanzados), lista de interfaces para características de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789244"
---
# <a name="overview-of-networking-interfaces"></a>Información general de las interfaces de red

Las características de red de este SDK se admiten a través de métodos de las interfaces siguientes.



| Interfaz                                                  | Descripción                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | Obtiene información acerca de los clientes conectados a un receptor de red.                                                                                       |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | Proporciona un método para obtener información acerca de un cliente conectado a un receptor de red del escritor. Esta interfaz extiende la interfaz **IWMClientConnections** . |
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | Proporciona un método de devolución de llamada para adquirir las credenciales de usuario al obtener acceso a un sitio remoto.                                                                  |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | Proporciona métodos avanzados en el objeto de lector.                                                                                                       |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | Extiende la interfaz **IWMReaderAdvanced2** .                                                                                                         |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | Extiende la interfaz **IWMReaderAdvanced3** .                                                                                                         |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | Configura las opciones de red en el objeto de lector.                                                                                                 |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | Configura opciones de red adicionales en el objeto de lector. Esta interfaz extiende la interfaz **IWMReaderNetworkConfig** .                         |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | Configura el objeto de receptor de red, que se utiliza para escribir medios digitales en una red.                                                                |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | Configura el objeto de receptor de la extracción, que se utiliza para distribuir medios digitales a puntos de publicación.                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de la funcionalidad de red**](implementing-network-functionality.md)
</dt> </dl>

 

 




