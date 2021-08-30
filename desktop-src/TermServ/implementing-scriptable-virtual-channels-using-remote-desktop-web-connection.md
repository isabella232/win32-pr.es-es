---
title: Implementación de canales virtuales que pueden incluirse en scripts mediante Conexión web a Escritorio remoto
description: Ejemplos de código que muestran los pasos para implementar canales virtuales que pueden incluirse en scripts con Conexión web a Escritorio remoto.
ms.assetid: a482b84d-96b6-4f42-8841-7039a1882789
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ba02fb745fb00d36d89011ce95255127caa9c9cf9c58873c5168df5114d72f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990705"
---
# <a name="implementing-scriptable-virtual-channels-by-using-remote-desktop-web-connection"></a>Implementación de canales virtuales que pueden incluirse en scripts mediante Conexión web a Escritorio remoto

En los siguientes ejemplos de código y procedimiento se muestran los pasos para implementar canales virtuales que pueden incluirse en scripts Conexión web a Escritorio remoto. Los ejemplos se escribieron en Visual Basic Scripting Edition y se supone que el control Escritorio remoto ActiveX se denomina "MsRdpClient".

**Para crear e implementar canales virtuales que pueden incluirse en scripts**

1.  Implemente el lado servidor de la aplicación y asegúrese de que se ejecuta en el Escritorio remoto host de sesión de escritorio remoto. Para obtener información sobre cómo implementar aplicaciones de canales virtuales en el servidor, vea [Aplicación de servidor de canal virtual](virtual-channel-server-application.md).
2.  En el script de cliente, llame a [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md)y pase una cadena que contenga una lista separada por comas de nombres de canal virtual.

    ```VB
    MsRdpClient.CreateVirtualChannels("mychan1,mychan2")
    ```

    

    Para obtener información sobre las restricciones de nomenclatura de canales virtuales, vea [Registro de cliente de canal virtual.](virtual-channel-client-registration.md)

3.  Llame [**a IMsTscAx::Conectar**](imstscax-connect.md) para crear la Servicios de Escritorio remoto conexión.

    ```VB
    MsRdpClient.connect
    ```

    

4.  Use el [**método IMsTscAx::SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md) para enviar datos al servidor, pasando una cadena que contiene el nombre del canal virtual y una segunda cadena que contiene los datos que se pasarán.

    ```VB
    MsRdpClient.SendOnVirtualChannel("mychan1","hello from the client")
    ```

    

5.  Reciba datos del servidor en el [**evento IMsTscAxEvents::OnChannelReceivedData.**](imstscaxevents-onchannelreceiveddata.md)

    ```VB
    Sub MsRdpClient.OnChannelReceivedData(chanName,data)
    Msgbox("received data:" &data& "on virtual channel:" &chanName)
    End sub
    ```

    

 

 




