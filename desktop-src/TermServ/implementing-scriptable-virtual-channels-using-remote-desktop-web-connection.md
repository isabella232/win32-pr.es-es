---
title: Implementación de canales virtuales con scripts mediante Conexión web a Escritorio remoto
description: Ejemplos de código que muestran los pasos para implementar canales virtuales que admiten scripts con Conexión web a Escritorio remoto.
ms.assetid: a482b84d-96b6-4f42-8841-7039a1882789
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a36f685de01312a93df67deb6be16ce031794c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777754"
---
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a><span data-ttu-id="ff54e-103">Implementación de canales virtuales con scripts mediante Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="ff54e-103">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>

<span data-ttu-id="ff54e-104">En el procedimiento y los ejemplos de código siguientes se muestran los pasos para implementar canales virtuales que admiten scripts con Conexión web a Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ff54e-104">The following procedure and code examples show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span> <span data-ttu-id="ff54e-105">Los ejemplos se escribieron en Visual Basic Scripting Edition y suponen que el control ActiveX Escritorio remoto se denomina "MsRdpClient".</span><span class="sxs-lookup"><span data-stu-id="ff54e-105">The examples were written in Visual Basic Scripting Edition and assume that the Remote Desktop ActiveX control is named "MsRdpClient".</span></span>

<span data-ttu-id="ff54e-106">**Para crear e implementar canales virtuales con scripts**</span><span class="sxs-lookup"><span data-stu-id="ff54e-106">**To create and deploy scriptable virtual channels**</span></span>

1.  <span data-ttu-id="ff54e-107">Implemente el lado servidor de la aplicación y asegúrese de que se está ejecutando en el servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="ff54e-107">Deploy the server side of the application and make sure it is running on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="ff54e-108">Para obtener información sobre la implementación de aplicaciones de canales virtuales en el servidor, consulte [aplicación de servidor de canal virtual](virtual-channel-server-application.md).</span><span class="sxs-lookup"><span data-stu-id="ff54e-108">For information about deploying virtual channels applications on the server, see [Virtual Channel Server Application](virtual-channel-server-application.md).</span></span>
2.  <span data-ttu-id="ff54e-109">En el script de cliente, llame a [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md), pasando una cadena que contenga una lista separada por comas de nombres de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="ff54e-109">In your client script, call [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md), passing a string that contains a comma-separated list of virtual channel names.</span></span>

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    <span data-ttu-id="ff54e-110">Para obtener información sobre las restricciones de nomenclatura de canal virtual, consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md).</span><span class="sxs-lookup"><span data-stu-id="ff54e-110">For information about virtual channel naming restrictions, see [Virtual Channel Client Registration](virtual-channel-client-registration.md).</span></span>

3.  <span data-ttu-id="ff54e-111">Llame a [**IMsTscAx:: Connect**](imstscax-connect.md) para crear la conexión servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="ff54e-111">Call [**IMsTscAx::Connect**](imstscax-connect.md) to create your Remote Desktop Services connection.</span></span>

    ```VB
    MsRdpClient.connect
    ```

    

4.  <span data-ttu-id="ff54e-112">Use el método [**IMsTscAx:: SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) para enviar datos al servidor, pasando una cadena que contiene el nombre del canal virtual y una segunda cadena que contiene los datos que se van a pasar.</span><span class="sxs-lookup"><span data-stu-id="ff54e-112">Use the [**IMsTscAx::SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) method to send data to the server, passing a string that contains the virtual channel name and a second string that contains the data to be passed.</span></span>

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  <span data-ttu-id="ff54e-113">Recibir datos del servidor en el evento [**IMsTscAxEvents:: OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) .</span><span class="sxs-lookup"><span data-stu-id="ff54e-113">Receive data from the server on the [**IMsTscAxEvents::OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) event.</span></span>

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




