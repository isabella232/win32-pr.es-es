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
# <a name="accepting-a-connection-remote-desktop-services"></a><span data-ttu-id="82c77-103">Aceptación de una conexión (Servicios de Escritorio remoto)</span><span class="sxs-lookup"><span data-stu-id="82c77-103">Accepting a Connection (Remote Desktop Services)</span></span>

<span data-ttu-id="82c77-104">En algún momento, el cliente del canal virtual dinámico (DVC) solicitará una conexión con el agente de escucha de DVC.</span><span class="sxs-lookup"><span data-stu-id="82c77-104">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span> <span data-ttu-id="82c77-105">Cuando esto ocurre, el agente de escucha puede generar un canal de comunicación único en el cliente, que se controla mediante el método [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) de [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span><span class="sxs-lookup"><span data-stu-id="82c77-105">When this occurs, the listener can spawn a unique communication channel to the client, which is handled by the [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) method of [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span></span> <span data-ttu-id="82c77-106">Para obtener un ejemplo, vea la implementación de **CDVCSamplePlugin:: OnNewChannelConnection** en el código de [ejemplo del complemento de cliente de DVC](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="82c77-106">For an example, see the implementation of **CDVCSamplePlugin::OnNewChannelConnection** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

<span data-ttu-id="82c77-107">En la ilustración siguiente se muestra la secuencia de eventos para establecer una conexión de DVC.</span><span class="sxs-lookup"><span data-stu-id="82c77-107">The following figure shows the sequence of events for establishing a DVC connection.</span></span> <span data-ttu-id="82c77-108">Los objetos sombreados son proporcionados por el usuario (aplicación/servicio de DVC y [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), mientras que los objetos sin sombreado forman parte del servicio (escritorio remoto host de sesión de escritorio remoto), el agente de escucha y el [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)de trabajo.</span><span class="sxs-lookup"><span data-stu-id="82c77-108">The shaded objects are user-supplied (DVC application/service and [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), while the un-shaded objects are part of the framework (Remote Desktop Session Host (RD Session Host) service, listener, and [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span></span>

![secuencia de eventos para establecer una conexión de DVC](images/acceptingconnection.png)

> [!Note]  
> <span data-ttu-id="82c77-110">En esta ilustración se supone que se ha creado un objeto de escucha mediante una llamada a [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) a [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)y que el complemento ha especificado [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) como parámetro.</span><span class="sxs-lookup"><span data-stu-id="82c77-110">This figure assumes that a listener object has been created through a [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) call to [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager), and that the plug-in has specified [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) as a parameter.</span></span>

 

 

 




