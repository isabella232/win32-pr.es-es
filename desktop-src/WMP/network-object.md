---
title: Objeto de red
description: El objeto Network proporciona propiedades y métodos que se usan para acceder a estadísticas relacionadas con la calidad de una conexión de red y para especificar y recuperar la configuración del proxy de red.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Objetos de red Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bf91c23d6a5c581430b17a370e66027a5f9174d0511a2647fba33834ec6c4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996115"
---
# <a name="network-object"></a>Objeto de red

El **objeto Network** proporciona propiedades y métodos que se usan para acceder a estadísticas relacionadas con la calidad de una conexión de red y para especificar y recuperar la configuración del proxy de red.

El **objeto Network** admite las siguientes propiedades.



| Propiedad                                           | Descripción                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Banda](network-bandwidth.md)                 | Recupera el ancho de banda actual del elemento multimedia.                                          |
| [Bitrate](network-bitrate.md)                     | Recupera la velocidad de bits actual que se recibe.                                              |
| [bufferingCount](network-bufferingcount.md)       | Recupera el número de veces que se produjo el almacenamiento en búfer durante la reproducción.                           |
| [bufferingProgress](network-bufferingprogress.md) | Recupera el porcentaje de almacenamiento en búfer completado.                                            |
| [bufferingTime](network-bufferingtime.md)         | Especifica o recupera la cantidad de tiempo de almacenamiento en búfer en milisegundos antes de que comience la reproducción. |
| [downloadProgress](network-downloadprogress.md)   | Recupera el porcentaje de descarga completada.                                             |
| [encodedFrameRate](network-encodedframerate.md)   | Recupera la velocidad de fotogramas de vídeo especificada por el autor del contenido.                             |
| [Framerate](network-framerate.md)                 | Recupera la velocidad de fotogramas de vídeo actual.                                                     |
| [framesSkipped](network-framesskipped.md)         | Recupera el número total de fotogramas omitido durante la reproducción.                               |
| [lostPackets](network-lostpackets.md)             | Recupera el número de paquetes perdidos.                                                       |
| [maxBandwidth](network-maxbandwidth.md)           | Especifica o recupera el ancho de banda máximo permitido.                                       |
| [maxBitRate](network-maxbitrate.md)               | Recupera la velocidad de bits de vídeo máxima posible.                                              |
| [receivedPackets](network-receivedpackets.md)     | Recupera el número de paquetes recibidos.                                                   |
| [receptionQuality](network-receptionquality.md)   | Recupera el porcentaje de paquetes recibidos en los últimos 30 segundos.                        |
| [recoveredPackets](network-recoveredpackets.md)   | Recupera el número de paquetes recuperados.                                                  |
| [sourceProtocol](network-sourceprotocol.md)       | Recupera el protocolo de origen utilizado para recibir datos.                                         |



 

El **objeto Network** admite los métodos siguientes.



| Método                                                       | Descripción                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [getProxyBypassForLocal](network-getproxybypassforlocal.md) | Recupera un valor que indica si el servidor proxy debe omitirse si el servidor de origen está en una red local. |
| [getProxyExceptionList](network-getproxyexceptionlist.md)   | Recupera la lista de excepciones de proxy.                                                                                  |
| [getProxyName](network-getproxyname.md)                     | Recupera el nombre de un servidor proxy que se usará.                                                                         |
| [getProxyPort](network-getproxyport.md)                     | Recupera el puerto de proxy que se usará.                                                                                     |
| [getProxySettings](network-getproxysettings.md)             | Recupera la configuración de proxy para un protocolo determinado.                                                                    |
| [setProxyBypassForLocal](network-setproxybypassforlocal.md) | Especifica un valor que indica si el servidor proxy debe omitirse si el servidor de origen está en una red local. |
| [setProxyExceptionList](network-setproxyexceptionlist.md)   | Especifica la lista de excepciones de proxy.                                                                                  |
| [setProxyName](network-setproxyname.md)                     | Especifica el nombre de un servidor proxy que se usará.                                                                         |
| [setProxyPort](network-setproxyport.md)                     | Especifica el puerto de proxy que se usará.                                                                                     |
| [setProxySettings](network-setproxysettings.md)             | Especifica la configuración de proxy para un protocolo determinado.                                                                    |



 

Se **tiene acceso** al objeto Network a través de la propiedad siguiente.



| Object                      | Propiedad                      |
|-----------------------------|-------------------------------|
| [Reproductor](player-object.md) | [network](player-network.md) |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




