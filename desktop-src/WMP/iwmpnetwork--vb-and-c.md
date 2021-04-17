---
title: Interfaz IWMPNetwork (VB y C) (WMP. h)
description: Proporciona propiedades y métodos para obtener acceso a las estadísticas relacionadas con la calidad de una conexión de red, y para especificar y recuperar la configuración del proxy de red. La interfaz IWMPNetwork expone las siguientes propiedades.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- IWMPNetwork (VB y C) interfaz de Windows Media Player
- IWMPNetwork (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 301fe5c89d2eb5df3dd4c22927e75a5607e7abd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690367"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a>Interfaz IWMPNetwork (VB y C#)

Proporciona propiedades y métodos para obtener acceso a las estadísticas relacionadas con la calidad de una conexión de red, y para especificar y recuperar la configuración del proxy de red.

La interfaz **IWMPNetwork** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La interfaz **IWMPNetwork (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IWMPNetwork (VB y C#)** tiene estos métodos.



| Método                                                                                           | Descripción                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**getProxyBypassForLocal**](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | Devuelve un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.<br/> |
| [**getProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | Devuelve la lista de excepciones de proxy.<br/>                                                                           |
| [**getProxyName**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | Devuelve el nombre del servidor proxy que se está usando.<br/>                                                            |
| [**getProxyPort**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | Devuelve el puerto del proxy que se está usando.<br/>                                                                          |
| [**getProxySettings**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | Devuelve información acerca de la configuración de proxy para un protocolo.<br/>                                                |
| [**setProxyBypassForLocal**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | Especifica si el servidor proxy se omite si el servidor de origen está en una red local.<br/>                  |
| [**setProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | Especifica la lista de excepciones de proxy.<br/>                                                                         |
| [**setProxyName**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | Especifica el nombre del servidor proxy que se va a usar.<br/>                                                              |
| [**setProxyPort**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | Especifica el puerto del proxy que se va a usar.<br/>                                                                            |
| [**setProxySettings**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | Especifica la configuración de proxy para un protocolo.<br/>                                                                |



 

### <a name="properties"></a>Propiedades

La interfaz **IWMPNetwork (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                          | Tipo de acceso           | Descripción                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [**Consumo**](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | Solo lectura<br/>  | Obtiene el ancho de banda actual del elemento multimedia.<br/>                                     |
| [**Velocidad**](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | Solo lectura<br/>  | Obtiene la velocidad de bits actual recibida.<br/>                                         |
| [**bufferingCount**](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | Solo lectura<br/>  | Obtiene el número de veces que se ha producido el almacenamiento en búfer durante la reproducción.<br/>                      |
| [**bufferingProgress**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | Solo lectura<br/>  | Obtiene el porcentaje de almacenamiento en búfer completado.<br/>                                       |
| [**bufferingTime**](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | Lectura/escritura<br/> | Obtiene o establece la cantidad de tiempo de almacenamiento en búfer en milisegundos antes de que comience la reproducción.<br/> |
| [**downloadProgress**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | Solo lectura<br/>  | Obtiene el porcentaje de descarga completada.<br/>                                     |
| [**encodedFrameRate**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | Solo lectura<br/>  | Obtiene la velocidad de fotogramas de vídeo especificada por el autor del contenido.<br/>                        |
| [**Velocidad**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | Solo lectura<br/>  | Obtiene la velocidad de fotogramas de vídeo actual.<br/>                                                |
| [**framesSkipped**](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | Solo lectura<br/>  | Obtiene el número total de fotogramas omitidos durante la reproducción.<br/>                          |
| [**lostPackets**](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | Solo lectura<br/>  | Obtiene el número de paquetes perdidos.<br/>                                                  |
| [**maxBandwidth**](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece el ancho de banda máximo permitido.<br/>                                       |
| [**maxBitRate**](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | Solo lectura<br/>  | Obtiene la velocidad de bits de vídeo máxima posible.<br/>                                         |
| [**receivedPackets**](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | Solo lectura<br/>  | Obtiene el número de paquetes recibidos.<br/>                                              |
| [**receptionQuality**](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | Solo lectura<br/>  | Obtiene el porcentaje de paquetes no perdidos en los últimos 30 segundos.<br/>                   |
| [**recoveredPackets**](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | Solo lectura<br/>  | Obtiene el número de paquetes recuperados.<br/>                                             |
| [**sourceProtocol**](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | Solo lectura<br/>  | Obtiene el protocolo de origen utilizado para recibir los datos.<br/>                                    |



 

Obtenga una interfaz **IWMPNetwork** con la siguiente propiedad.



| Object                                                                   | Propiedad                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Storage**](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





