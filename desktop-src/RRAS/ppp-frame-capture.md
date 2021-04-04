---
title: Escritura de un controlador para capturar tramas PPP
description: En este documento se explica cómo desarrollar un controlador que pueda capturar tramas PPP en Windows vista antes de que se compriman o cifren en la ruta de acceso de envío o después de que se descomprimen o descifran en la ruta de acceso de recepción.
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d592596674cd64af5122303afefcfc81026dad27
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077367"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a>Escritura de un controlador para capturar tramas PPP

Cuando los fotogramas de Protocolo punto a punto (PPP) se envían a través de un túnel del Protocolo de túnel punto a punto (PPTP) con cifrado activado, o a través de un túnel del Protocolo de túnel de capa 2 (L2TP) que usa IPSec para el cifrado, la utilidad de captura de tramas PPP típica solo puede capturar tramas PPP que tengan un campo de identidad de protocolo cifra En este documento se explica cómo desarrollar un controlador que pueda capturar tramas PPP en Windows vista antes de que se compriman o cifren en la ruta de acceso de envío o después de que se descomprimen o descifran en la ruta de acceso de recepción.

1.  Escribir un controlador de protocolo NDIS. Para obtener más información, consulte [controladores de protocolo ndis 6,0](https://msdn.microsoft.com/library/ms795570.aspx) o controladores de [Protocolo ndis (NDIS 5,1)](https://msdn.microsoft.com/library/ms801145.aspx).
2.  Instale el controlador con una identidad de hardware de "MS \_ Netmon". Para obtener instrucciones detalladas sobre cómo instalar el controlador con una identidad de hardware específica, consulte la [sección modelos de INF](https://msdn.microsoft.com/library/ms794357.aspx).
    > [!Note]  
    > Cada máquina de Windows Vista permite la instalación de una sola entidad de controlador que tiene la \_ identidad de hardware "MS Netmon". Para instalar otro controlador con esta identidad, se debe desinstalar el primer controlador. Un controlador que se instala sin usar la identidad de \_ hardware "MS Netmon" no puede realizar el enlace necesario para capturar tramas ppp.

     

3.  El controlador de protocolo debe especificar "ndiswanbh" como la interfaz de enlace para capturar tramas PPP. Para obtener instrucciones detalladas, consulte [especificar interfaces de enlace](https://msdn.microsoft.com/library/aa937923.aspx).
4.  La implementación de [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) en el controlador debe admitir "NdisMediumWan" como parte de la matriz mediana, de modo que pueda abrir el perímetro del minipuerto ndiswanbh mediante la función [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) .
5.  Si se llama a la función [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) con el estado NDIS \_ \_ Success Success, el controlador de protocolo debe establecer el OID del [ \_ \_ \_ \_ filtro de paquetes actual de OID gen](https://msdn.microsoft.com/library/bb314089.aspx) con el tipo de paquete de paquetes [NDIS \_ \_ \_ promiscuo](https://msdn.microsoft.com/library/bb314089.aspx) y el [tipo de \_ paquete NDIS \_ \_ \_ local](https://msdn.microsoft.com/library/bb314089.aspx) a través de este enlace. Una vez hecho esto, el controlador de protocolo recibirá los fotogramas PPP descifrados de la capa de tramas PPP en su función [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) .

> [!Note]  
> Esta información solo se aplica a los controladores de un equipo con Windows Vista.

 

 

 




