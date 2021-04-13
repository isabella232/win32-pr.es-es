---
title: Inicio de un agente de escucha de DVC
description: Para establecer una conexión correcta entre dos módulos de canal virtual dinámico (DVC) que se ejecutan en el cliente y servidor de Conexión a Escritorio remoto (RDC), un agente de escucha de DVC debe estar en ejecución y en un estado de escucha.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b625d5547facd0487af170af9d59eddd6bfed87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357700"
---
# <a name="starting-a-dvc-listener"></a><span data-ttu-id="8c51a-103">Inicio de un agente de escucha de DVC</span><span class="sxs-lookup"><span data-stu-id="8c51a-103">Starting a DVC Listener</span></span>

<span data-ttu-id="8c51a-104">Para establecer una conexión correcta entre dos módulos de canal virtual dinámico (DVC) que se ejecutan en el cliente y servidor de Conexión a Escritorio remoto (RDC), un agente de escucha de DVC debe estar en ejecución y en un estado de escucha.</span><span class="sxs-lookup"><span data-stu-id="8c51a-104">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

<span data-ttu-id="8c51a-105">La creación de instancias de un agente de escucha suele producirse en el método [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) del complemento DVC.</span><span class="sxs-lookup"><span data-stu-id="8c51a-105">The instantiation of a listener typically occurs in the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of the DVC plug-in.</span></span> <span data-ttu-id="8c51a-106">Sin embargo, la creación de instancias no se limita al método **Initialize** y se puede iniciar en cualquier punto de la ejecución del complemento.</span><span class="sxs-lookup"><span data-stu-id="8c51a-106">However, instantiation is not limited to the **Initialize** method, and can be started at any point of the plug-in execution.</span></span> <span data-ttu-id="8c51a-107">El agente de escucha se describe mediante la interfaz [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) con la que se crea una instancia de [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span><span class="sxs-lookup"><span data-stu-id="8c51a-107">The listener is described by the [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) interface which is instantiated by the [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="8c51a-108">Una instancia del administrador de canales se pasa al complemento en el punto de inicialización.</span><span class="sxs-lookup"><span data-stu-id="8c51a-108">An instance to the channel manager is passed to the plug-in at the initialization point.</span></span> <span data-ttu-id="8c51a-109">El complemento puede mantener una referencia interna a la instancia siempre que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8c51a-109">The plug-in can maintain an internal reference to the instance as long as it needs to.</span></span>

<span data-ttu-id="8c51a-110">Un complemento puede crear instancias de todos los agentes de escucha que necesite.</span><span class="sxs-lookup"><span data-stu-id="8c51a-110">A plug-in can instantiate as many listeners as it needs to.</span></span> <span data-ttu-id="8c51a-111">Las conexiones entrantes se controlarán mediante [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), que se proporciona en el método [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) de [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span><span class="sxs-lookup"><span data-stu-id="8c51a-111">Any incoming connection will be handled by [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), which is supplied in the [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) method of [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="8c51a-112">Para obtener un ejemplo, vea la implementación de **CDVCSamplePlugin:: Initialize** en el ejemplo de código de [ejemplo del complemento de cliente de DVC](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="8c51a-112">For an example, see the implementation of **CDVCSamplePlugin::Initialize** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

 

 




