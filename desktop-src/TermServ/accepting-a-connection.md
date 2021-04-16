---
title: Aceptación de una conexión (Servicios de Escritorio remoto)
description: En algún momento, el cliente del canal virtual dinámico (DVC) solicitará una conexión con el agente de escucha de DVC.
ms.assetid: eab17aa9-590c-4da2-a1a9-6e50a11d1de7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13aa0b78e459c85e7ba07e043e3da313b3f6118
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104551607"
---
# <a name="accepting-a-connection-remote-desktop-services"></a>Aceptación de una conexión (Servicios de Escritorio remoto)

En algún momento, el cliente del canal virtual dinámico (DVC) solicitará una conexión con el agente de escucha de DVC. Cuando esto ocurre, el agente de escucha puede generar un canal de comunicación único en el cliente, que se controla mediante el método [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) de [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback). Para obtener un ejemplo, vea la implementación de **CDVCSamplePlugin:: OnNewChannelConnection** en el código de [ejemplo del complemento de cliente de DVC](dvc-client-plug-in-example.md) .

En la ilustración siguiente se muestra la secuencia de eventos para establecer una conexión de DVC. Los objetos sombreados son proporcionados por el usuario (aplicación/servicio de DVC y [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), mientras que los objetos sin sombreado forman parte del servicio (escritorio remoto host de sesión de escritorio remoto), el agente de escucha y el [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)de trabajo.

![secuencia de eventos para establecer una conexión de DVC](images/acceptingconnection.png)

> [!Note]  
> En esta ilustración se supone que se ha creado un objeto de escucha mediante una llamada a [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) a [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)y que el complemento ha especificado [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) como parámetro.

 

 

 




