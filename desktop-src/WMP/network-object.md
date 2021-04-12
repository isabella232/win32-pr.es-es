---
title: Objeto de red
description: El objeto de red proporciona las propiedades y los métodos utilizados para obtener acceso a las estadísticas relacionadas con la calidad de una conexión de red, y para especificar y recuperar la configuración del proxy de red.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Media Player de objetos de red de Windows
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d439679636bce773c43f5610060c4744ef4d5d7c
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2019
ms.locfileid: "104419765"
---
# <a name="network-object"></a>Objeto de red

El objeto de **red** proporciona las propiedades y los métodos utilizados para obtener acceso a las estadísticas relacionadas con la calidad de una conexión de red, y para especificar y recuperar la configuración del proxy de red.

El objeto de **red** admite las siguientes propiedades.



| Propiedad                                           | Descripción                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Consumo](network-bandwidth.md)                 | Recupera el ancho de banda actual del elemento multimedia.                                          |
| [Velocidad](network-bitrate.md)                     | Recupera la velocidad de bits actual recibida.                                              |
| [bufferingCount](network-bufferingcount.md)       | Recupera el número de veces que se ha producido el almacenamiento en búfer durante la reproducción.                           |
| [bufferingProgress](network-bufferingprogress.md) | Recupera el porcentaje de almacenamiento en búfer completado.                                            |
| [bufferingTime](network-bufferingtime.md)         | Especifica o recupera la cantidad de tiempo de almacenamiento en búfer en milisegundos antes de que comience la reproducción. |
| [downloadProgress](network-downloadprogress.md)   | Recupera el porcentaje de descarga completada.                                             |
| [encodedFrameRate](network-encodedframerate.md)   | Recupera la velocidad de fotogramas de vídeo especificada por el autor del contenido.                             |
| [Velocidad](network-framerate.md)                 | Recupera la velocidad de fotogramas de vídeo actual.                                                     |
| [framesSkipped](network-framesskipped.md)         | Recupera el número total de fotogramas omitidos durante la reproducción.                               |
| [lostPackets](network-lostpackets.md)             | Recupera el número de paquetes perdidos.                                                       |
| [maxBandwidth](network-maxbandwidth.md)           | Especifica o recupera el ancho de banda máximo permitido.                                       |
| [maxBitRate](network-maxbitrate.md)               | Recupera la velocidad de bits de vídeo máxima posible.                                              |
| [receivedPackets](network-receivedpackets.md)     | Recupera el número de paquetes recibidos.                                                   |
| [receptionQuality](network-receptionquality.md)   | Recupera el porcentaje de paquetes recibidos en los últimos 30 segundos.                        |
| [recoveredPackets](network-recoveredpackets.md)   | Recupera el número de paquetes recuperados.                                                  |
| [sourceProtocol](network-sourceprotocol.md)       | Recupera el protocolo de origen usado para recibir los datos.                                         |



 

El objeto de **red** admite los métodos siguientes.



| Método                                                       | Descripción                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [getProxyBypassForLocal](network-getproxybypassforlocal.md) | Recupera un valor que indica si el servidor proxy se debe omitir si el servidor de origen está en una red local. |
| [getProxyExceptionList](network-getproxyexceptionlist.md)   | Recupera la lista de excepciones del proxy.                                                                                  |
| [getProxyName](network-getproxyname.md)                     | Recupera el nombre de un servidor proxy que se va a usar.                                                                         |
| [getProxyPort](network-getproxyport.md)                     | Recupera el puerto del proxy que se va a usar.                                                                                     |
| [getProxySettings](network-getproxysettings.md)             | Recupera la configuración del proxy para un protocolo determinado.                                                                    |
| [setProxyBypassForLocal](network-setproxybypassforlocal.md) | Especifica un valor que indica si el servidor proxy debe omitirse si el servidor de origen está en una red local. |
| [setProxyExceptionList](network-setproxyexceptionlist.md)   | Especifica la lista de excepciones de proxy.                                                                                  |
| [setProxyName](network-setproxyname.md)                     | Especifica el nombre de un servidor proxy que se va a usar.                                                                         |
| [setProxyPort](network-setproxyport.md)                     | Especifica el puerto del proxy que se va a usar.                                                                                     |
| [setProxySettings](network-setproxysettings.md)             | Especifica la configuración de proxy para un protocolo determinado.                                                                    |



 

Se tiene acceso al objeto de **red** a través de la siguiente propiedad.



| Object                      | Propiedad                      |
|-----------------------------|-------------------------------|
| [Reproductor](player-object.md) | [network](player-network.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




