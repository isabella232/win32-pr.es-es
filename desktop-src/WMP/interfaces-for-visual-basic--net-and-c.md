---
title: Interfaces para Visual Basic .NET y C
description: Interfaces para Visual Basic .NET y C \
ms.assetid: c66f1e03-20eb-45b1-8710-be9eae63e7ad
keywords:
- Windows Media Player, interfaces
- Windows Media Player Mobile, interfaces
- Modelo de objetos de Windows Media Player, interfaces
- modelo de objetos, interfaces
- Control ActiveX, interfaces
- Control ActiveX de Windows Media Player, interfaces
- Control ActiveX móvil de Windows Media Player, interfaces
- Referencia del modelo de objetos, interfaces
- Referencia del modelo de objetos de interfaz
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a301cb075ccee049272f1db9b2582aeae6697fa3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269046"
---
# <a name="interfaces-for-visual-basic-net-and-c"></a>Interfaces para Visual Basic .NET y C #

En esta sección se documentan las interfaces expuestas por el control ActiveX de Windows Media Player.

Se usan varias propiedades y métodos del [objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) para recuperar interfaces específicas. Estas interfaces, a su vez, pueden tener propiedades y métodos de descriptor de acceso para recuperar otras interfaces.

El control Windows Media Player expone las siguientes interfaces.



| Interfaz                                                      | Descripción                                                                                                                                                       |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IWMPCdrom](iwmpcdrom--vb-and-c.md)                           | Obtiene acceso a un CD o DVD de una unidad.                                                                                                                                  |
| [IWMPCdromBurn](iwmpcdromburn--vb-and-c.md)                   | Proporciona propiedades y métodos para administrar la creación de CDs de audio.                                                                                                     |
| [IWMPCdromCollection](iwmpcdromcollection--vb-and-c.md)       | Obtiene acceso a una colección de unidades de CD o DVD.                                                                                                                        |
| [IWMPCdromRip](iwmpcdromrip--vb-and-c.md)                     | Proporciona propiedades y métodos para administrar las pistas de *copia o copia desde un* CD de audio.                                                                         |
| [IWMPClosedCaption](iwmpclosedcaption--vb-and-c.md)           | Proporciona una manera de incluir leyendas con un archivo multimedia digital.                                                                                                     |
| [IWMPClosedCaption2](iwmpclosedcaption2--vb-and-c.md)         | Proporciona propiedades y métodos adicionales de subtítulos (CC).                                                                                                     |
| [IWMPControls](iwmpcontrols--vb-and-c.md)                     | Representa los controles de transporte de Windows Media Player, como reproducir, detener y pausar.                                                                         |
| [IWMPControls2](iwmpcontrols2--vb-and-c.md)                   | Proporciona un método de control adicional para inmovilizar la reproducción en el fotograma siguiente o anterior.                                                                           |
| [IWMPControls3](iwmpcontrols3--vb-and-c.md)                   | Proporciona propiedades y métodos de control adicionales para la selección y compatibilidad del lenguaje de audio.                                                                      |
| [IWMPDVD](iwmpdvd--vb-and-c.md)                               | Proporciona propiedades y métodos para trabajar con DVDs.                                                                                                            |
| [IWMPError](iwmperror--vb-and-c.md)                           | Obtiene acceso a una colección de interfaces [IWMPErrorItem](iwmperroritem--vb-and-c.md) para recuperar información de errores.                                                |
| [IWMPErrorItem](iwmperroritem--vb-and-c.md)                   | Proporciona acceso a la información de error.                                                                                                                             |
| [IWMPErrorItem2](iwmperroritem2--vb-and-c.md)                 | Proporciona una propiedad de elemento de error adicional para obtener un código de condición de error.                                                                                   |
| **IWMPFolderMonitorServices**                                  | No se admite para la programación de .NET.                                                                                                                               |
| [IWMPLibrary](iwmplibrary--vb-and-c.md)                       | Representa una biblioteca.                                                                                                                                             |
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md)       | Proporciona métodos para enumerar las bibliotecas.                                                                                                                          |
| **IWMPLibrarySharingServices**                                 | No se admite para la programación de .NET.                                                                                                                               |
| [IWMPMedia](iwmpmedia--vb-and-c.md)                           | Proporciona una manera de establecer y recuperar las propiedades de un elemento multimedia.                                                                                                |
| [IWMPMedia2](iwmpmedia2--vb-and-c.md)                         | Proporciona acceso a una propiedad de elemento multimedia adicional.                                                                                                             |
| [IWMPMedia3](iwmpmedia3--vb-and-c.md)                         | Proporciona métodos adicionales para tener acceso a las propiedades de un elemento multimedia.                                                                                             |
| [IWMPMediaCollection](iwmpmediacollection--vb-and-c.md)       | Proporciona métodos que se pueden utilizar para organizar una colección grande de elementos multimedia.                                                                                  |
| [IWMPMediaCollection2](iwmpmediacollection2--vb-and-c.md)     | Proporciona métodos que complementan la interfaz **IWMPMediaCollection** .                                                                                           |
| [IWMPMetadataPicture](iwmpmetadatapicture--vb-and-c.md)       | Proporciona propiedades para obtener información acerca de la imagen contenida en un archivo multimedia digital representado por un atributo de metadatos de **WM/imagen** .         |
| [IWMPMetadataText](iwmpmetadatatext--vb-and-c.md)             | Proporciona propiedades para obtener información sobre los atributos de metadatos de texto complejos.                                                                            |
| [IWMPNetwork](iwmpnetwork--vb-and-c.md)                       | Proporciona propiedades y métodos para obtener acceso a las estadísticas relacionadas con la calidad de una conexión de red, y para especificar y recuperar la configuración del proxy de red.     |
| **IWMPPlayerApplication**                                      | No se admite para la programación de .NET.                                                                                                                               |
| **IWMPPlayerServices**                                         | No se admite para la programación de .NET.                                                                                                                               |
| **IWMPPlayerServices2**                                        | No se admite para la programación de .NET.                                                                                                                               |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                     | Proporciona propiedades y métodos para organizar, administrar y manipular elementos multimedia en una lista de reproducción.                                                                    |
| [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md)           | Obtiene acceso a una colección de interfaces [IWMPPlaylist](iwmpplaylist--vb-and-c.md) por número de índice.                                                                   |
| [IWMPPlaylistCollection](iwmpplaylistcollection--vb-and-c.md) | Proporciona métodos para manipular interfaces [IWMPPlaylist](iwmpplaylist--vb-and-c.md) y [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md) en una colección. |
| [IWMPQuery](iwmpquery--vb-and-c.md)                           | Representa una consulta compuesta.                                                                                                                                      |
| [IWMPSettings](iwmpsettings--vb-and-c.md)                     | Proporciona propiedades y métodos que obtienen o establecen los valores de configuración de Windows Media Player.                                                                      |
| [IWMPSettings2](iwmpsettings2--vb-and-c.md)                   | Proporciona propiedades y un método que complementan la interfaz **IWMPSettings** .                                                                                  |
| [IWMPStringCollection](iwmpstringcollection--vb-and-c.md)     | Proporciona una propiedad y un método para tener acceso a una colección de cadenas por número de índice.                                                                           |
| [IWMPStringCollection2](iwmpstringcollection2--vb-and-c.md)   | Proporciona métodos que complementan la interfaz **IWMPStringCollection** .                                                                                          |
| **IWMPSyncDevice**                                             | No se admite para la programación de .NET.                                                                                                                               |
| **IWMPSyncDevice2**                                            | No se admite para la programación de .NET.                                                                                                                               |
| **IWMPSyncServices**                                           | No se admite para la programación de .NET.                                                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia del modelo de objetos para Visual Basic .NET y C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 




