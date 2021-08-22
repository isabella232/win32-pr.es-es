---
title: Interfaz IWMPNetwork (VB y C) (Wmp.h)
description: Proporciona propiedades y métodos para acceder a estadísticas relacionadas con la calidad de una conexión de red y para especificar y recuperar la configuración del proxy de red. La interfaz IWMPNetwork expone las siguientes propiedades.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- Interfaz IWMPNetwork (VB y C) Reproductor de Windows Media
- Interfaz IWMPNetwork (VB y C) Reproductor de Windows Media , descrita
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
ms.openlocfilehash: 93110b25bd7d194c4f1d7c213228512fd8bc6000df15b726e3f32a6e6e79a62a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572455"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a>Interfaz IWMPNetwork (VB y C#)

Proporciona propiedades y métodos para acceder a estadísticas relacionadas con la calidad de una conexión de red y para especificar y recuperar la configuración del proxy de red.

La **interfaz IWMPNetwork** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La **interfaz IWMPNetwork (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWMPNetwork (VB y C#)** tiene estos métodos.



| Método                                                                                           | Descripción                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**getProxyBypassForLocal**](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | Devuelve un valor que indica si se omite el servidor proxy si el servidor de origen está en una red local.<br/> |
| [**getProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | Devuelve la lista de excepciones de proxy.<br/>                                                                           |
| [**getProxyName**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | Devuelve el nombre del servidor proxy que se está utilizando.<br/>                                                            |
| [**getProxyPort**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | Devuelve el puerto de proxy que se está utilizando.<br/>                                                                          |
| [**getProxySettings**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | Devuelve información sobre la configuración de proxy de un protocolo.<br/>                                                |
| [**setProxyBypassForLocal**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | Especifica si se omite el servidor proxy si el servidor de origen está en una red local.<br/>                  |
| [**setProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | Especifica la lista de excepciones de proxy.<br/>                                                                         |
| [**setProxyName**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | Especifica el nombre del servidor proxy que se usará.<br/>                                                              |
| [**setProxyPort**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | Especifica el puerto de proxy que se usará.<br/>                                                                            |
| [**setProxySettings**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | Especifica la configuración de proxy para un protocolo.<br/>                                                                |



 

### <a name="properties"></a>Propiedades

La **interfaz IWMPNetwork (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                          | Tipo de acceso           | Descripción                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [**Banda**](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | Solo lectura<br/>  | Obtiene el ancho de banda actual del elemento multimedia.<br/>                                     |
| [**Bitrate**](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | Solo lectura<br/>  | Obtiene la velocidad de bits actual que se recibe.<br/>                                         |
| [**bufferingCount**](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | Solo lectura<br/>  | Obtiene el número de veces que se produjo el almacenamiento en búfer durante la reproducción.<br/>                      |
| [**bufferingProgress**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | Solo lectura<br/>  | Obtiene el porcentaje de almacenamiento en búfer completado.<br/>                                       |
| [**bufferingTime**](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | Lectura/escritura<br/> | Obtiene o establece la cantidad de tiempo de almacenamiento en búfer en milisegundos antes de que comience la reproducción.<br/> |
| [**downloadProgress**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | Solo lectura<br/>  | Obtiene el porcentaje de descarga completada.<br/>                                     |
| [**encodedFrameRate**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | Solo lectura<br/>  | Obtiene la velocidad de fotogramas de vídeo especificada por el autor del contenido.<br/>                        |
| [**Framerate**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | Solo lectura<br/>  | Obtiene la velocidad de fotogramas de vídeo actual.<br/>                                                |
| [**framesSkipped**](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | Solo lectura<br/>  | Obtiene el número total de fotogramas omitido durante la reproducción.<br/>                          |
| [**lostPackets**](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | Solo lectura<br/>  | Obtiene el número de paquetes perdidos.<br/>                                                  |
| [**maxBandwidth**](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | Lectura/escritura<br/> | Obtiene o establece el ancho de banda máximo permitido.<br/>                                       |
| [**maxBitRate**](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | Solo lectura<br/>  | Obtiene la velocidad de bits de vídeo máxima posible.<br/>                                         |
| [**receivedPackets**](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | Solo lectura<br/>  | Obtiene el número de paquetes recibidos.<br/>                                              |
| [**receptionQuality**](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | Solo lectura<br/>  | Obtiene el porcentaje de paquetes no perdidos en los últimos 30 segundos.<br/>                   |
| [**recoveredPackets**](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | Solo lectura<br/>  | Obtiene el número de paquetes recuperados.<br/>                                             |
| [**sourceProtocol**](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | Solo lectura<br/>  | Obtiene el protocolo de origen utilizado para recibir datos.<br/>                                    |



 

Obtenga una **interfaz IWMPNetwork** mediante la siguiente propiedad.



| Object                                                                   | Propiedad                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Red**](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





