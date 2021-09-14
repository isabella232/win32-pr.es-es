---
title: Información general de las interfaces de red
description: Información general de las interfaces de red
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows SDK de formato multimedia, interfaces de red
- Windows SDK de formato multimedia, interfaces
- Formato de sistemas avanzados (ASF), interfaces de red
- ASF (formato de sistemas avanzados), interfaces de red
- Formato de sistemas avanzados (ASF), lista de interfaces para características de red
- ASF (formato de sistemas avanzados), lista de interfaces para características de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266951"
---
# <a name="overview-of-networking-interfaces"></a>Información general de las interfaces de red

Las características de red de este SDK se admiten a través de los métodos de las interfaces siguientes.



| Interfaz                                                  | Descripción                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMClientConnections**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | Obtiene información sobre los clientes conectados a un receptor de red.                                                                                       |
| [**IWMClientConnections2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | Proporciona un método para obtener información sobre un cliente asociado a un receptor de red de escritor. Esta interfaz amplía la **interfaz IWMClientConnections.** |
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | Proporciona un método de devolución de llamada para adquirir credenciales de usuario al acceder a un sitio remoto.                                                                  |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | Proporciona métodos avanzados en el objeto de lector.                                                                                                       |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | Extiende la **interfaz IWMReaderAdvanced2.**                                                                                                         |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | Extiende la **interfaz IWMReaderAdvanced3.**                                                                                                         |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | Configura los valores de red en el objeto de lector.                                                                                                 |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | Configura opciones de red adicionales en el objeto de lector. Esta interfaz amplía la **interfaz IWMReaderNetworkConfig.**                         |
| [**IWMWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | Configura el objeto de receptor de red, que se usa para escribir medios digitales en una red.                                                                |
| [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | Configura el objeto receptor de inserción, que se usa para distribuir los medios digitales a los puntos de publicación.                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de la funcionalidad de red**](implementing-network-functionality.md)
</dt> </dl>

 

 




