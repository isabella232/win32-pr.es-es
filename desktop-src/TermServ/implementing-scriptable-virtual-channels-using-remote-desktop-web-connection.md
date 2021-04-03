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
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a>Implementación de canales virtuales con scripts mediante Conexión web a Escritorio remoto

En el procedimiento y los ejemplos de código siguientes se muestran los pasos para implementar canales virtuales que admiten scripts con Conexión web a Escritorio remoto. Los ejemplos se escribieron en Visual Basic Scripting Edition y suponen que el control ActiveX Escritorio remoto se denomina "MsRdpClient".

**Para crear e implementar canales virtuales con scripts**

1.  Implemente el lado servidor de la aplicación y asegúrese de que se está ejecutando en el servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto). Para obtener información sobre la implementación de aplicaciones de canales virtuales en el servidor, consulte [aplicación de servidor de canal virtual](virtual-channel-server-application.md).
2.  En el script de cliente, llame a [**IMsTscAx:: CreateVirtualChannels**](imstscax-createvirtualchannels.md), pasando una cadena que contenga una lista separada por comas de nombres de canal virtual.

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    Para obtener información sobre las restricciones de nomenclatura de canal virtual, consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md).

3.  Llame a [**IMsTscAx:: Connect**](imstscax-connect.md) para crear la conexión servicios de escritorio remoto.

    ```VB
    MsRdpClient.connect
    ```

    

4.  Use el método [**IMsTscAx:: SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) para enviar datos al servidor, pasando una cadena que contiene el nombre del canal virtual y una segunda cadena que contiene los datos que se van a pasar.

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  Recibir datos del servidor en el evento [**IMsTscAxEvents:: OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md) .

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




