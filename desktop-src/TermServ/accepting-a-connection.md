---
title: Aceptar una conexión (Servicios de Escritorio remoto)
description: En algún momento, el cliente del canal virtual dinámico (DVC) solicitará una conexión al agente de escucha de DVC.
ms.assetid: eab17aa9-590c-4da2-a1a9-6e50a11d1de7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13aa0b78e459c85e7ba07e043e3da313b3f6118
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073380"
---
# <a name="accepting-a-connection-remote-desktop-services"></a>Aceptar una conexión (Servicios de Escritorio remoto)

En algún momento, el cliente del canal virtual dinámico (DVC) solicitará una conexión al agente de escucha de DVC. Cuando esto ocurre, el agente de escucha puede generar un canal de comunicación único para el cliente, que se controla mediante el método [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) de [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback). Para obtener un ejemplo, vea la implementación de **CDVCSamplePlugin::OnNewChannelConnection** en el código de ejemplo del complemento de cliente [DVC.](dvc-client-plug-in-example.md)

En la ilustración siguiente se muestra la secuencia de eventos para establecer una conexión DVC. Los objetos sombreados son proporcionados por el usuario (aplicación/servicio DVC e [**IWTSListenerCallback),**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)mientras que los objetos sin sombreado forman parte del servicio de marco (host de sesión de Escritorio remoto (host de sesión de Escritorio remoto), agente de escucha e [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).

![secuencia de eventos para establecer una conexión dvc](images/acceptingconnection.png)

> [!Note]  
> En esta ilustración se supone que se ha creado un objeto de agente de escucha a través de una llamada [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) a [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)y que el complemento ha especificado [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) como parámetro.

 

 

 




