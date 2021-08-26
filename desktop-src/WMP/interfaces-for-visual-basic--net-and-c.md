---
title: Interfaces para Visual Basic .NET y C
description: Interfaces para Visual Basic .NET y C\
ms.assetid: c66f1e03-20eb-45b1-8710-be9eae63e7ad
keywords:
- Reproductor de Windows Media,interfaces
- Reproductor de Windows Media Mobile,interfaces
- Reproductor de Windows Media modelo de objetos,interfaces
- object model,interfaces
- ActiveX control,interfaces
- Reproductor de Windows Media ActiveX control,interfaces
- Reproductor de Windows Media Control de ActiveX móviles, interfaces
- referencia del modelo de objetos, interfaces
- Referencia del modelo de objetos de interfaz
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7024c60235b0a545463826fc8948adf3716c9c2d5b491414212d788087404b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862585"
---
# <a name="interfaces-for-visual-basic-net-and-c"></a>Interfaces para Visual Basic .NET y C #

En esta sección se documenta las interfaces expuestas por el control Reproductor de Windows Media ActiveX datos.

Se usan varias propiedades y métodos del objeto [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) para recuperar interfaces específicas. Estas interfaces, a su vez, pueden tener propiedades y métodos de accessor para recuperar más interfaces.

El control Reproductor de Windows Media expone las interfaces siguientes.



| Interfaz                                                      | Descripción                                                                                                                                                       |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IWMPCdrom](iwmpcdrom--vb-and-c.md)                           | Accede a un CD o DVD en una unidad.                                                                                                                                  |
| [IWMPCdrom (IWMPCdrom )](iwmpcdromburn--vb-and-c.md)                   | Proporciona propiedades y métodos para administrar la creación de CD de audio.                                                                                                     |
| [IWMPCdromCollection](iwmpcdromcollection--vb-and-c.md)       | Accede a una colección de unidades de CD o DVD.                                                                                                                        |
| [IWMPCdromRip](iwmpcdromrip--vb-and-c.md)                     | Proporciona propiedades y métodos para administrar la copia o *eliminación de* pistas desde un CD de audio.                                                                         |
| [IWMPClosedCaption](iwmpclosedcaption--vb-and-c.md)           | Proporciona una manera de incluir subtítulos con un archivo multimedia digital.                                                                                                     |
| [IWMPClosedCaption2](iwmpclosedcaption2--vb-and-c.md)         | Proporciona métodos y propiedades de subtítulos adicionales.                                                                                                     |
| [IWMPControls](iwmpcontrols--vb-and-c.md)                     | Representa los controles de transporte de Reproductor de Windows Media, como Reproducir, Detener y Pausar.                                                                         |
| [IWMPControls2](iwmpcontrols2--vb-and-c.md)                   | Proporciona un método de control adicional para inmovilizar la reproducción en el fotograma siguiente o anterior.                                                                           |
| [IWMPControls3](iwmpcontrols3--vb-and-c.md)                   | Proporciona propiedades y métodos de control adicionales para la selección y compatibilidad del idioma de audio.                                                                      |
| [IWMPDVD](iwmpdvd--vb-and-c.md)                               | Proporciona propiedades y métodos para trabajar con DVD.                                                                                                            |
| [IWMPError](iwmperror--vb-and-c.md)                           | Tiene acceso a una colección [de interfaces IWMPErrorItem](iwmperroritem--vb-and-c.md) para recuperar información de error.                                                |
| [IWMPErrorItem](iwmperroritem--vb-and-c.md)                   | Proporciona acceso a la información de error.                                                                                                                             |
| [IWMPErrorItem2](iwmperroritem2--vb-and-c.md)                 | Proporciona una propiedad de elemento de error adicional para obtener un código de condición de error.                                                                                   |
| **IWMPFolderMonitorServices**                                  | No se admite para la programación de .NET.                                                                                                                               |
| [IWMPLibrary](iwmplibrary--vb-and-c.md)                       | Representa una biblioteca.                                                                                                                                             |
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md)       | Proporciona métodos para enumerar bibliotecas.                                                                                                                          |
| **IWMPLibrarySharingServices**                                 | No se admite para la programación de .NET.                                                                                                                               |
| [IWMPMedia](iwmpmedia--vb-and-c.md)                           | Proporciona una manera de establecer y recuperar las propiedades de un elemento multimedia.                                                                                                |
| [IWMPMedia2](iwmpmedia2--vb-and-c.md)                         | Proporciona acceso a una propiedad de elemento multimedia adicional.                                                                                                             |
| [IWMPMedia3](iwmpmedia3--vb-and-c.md)                         | Proporciona métodos adicionales para tener acceso a las propiedades de un elemento multimedia.                                                                                             |
| [IWMPMediaCollection](iwmpmediacollection--vb-and-c.md)       | Proporciona métodos que se pueden usar para organizar una gran colección de elementos multimedia.                                                                                  |
| [IWMPMediaCollection2](iwmpmediacollection2--vb-and-c.md)     | Proporciona métodos que complementan **la interfaz IWMPMediaCollection.**                                                                                           |
| [IWMPMetadataPicture](iwmpmetadatapicture--vb-and-c.md)       | Proporciona propiedades para obtener información sobre la imagen contenida en un archivo multimedia digital representado por un **atributo de metadatos WM/Picture.**         |
| [IWMPMetadataText](iwmpmetadatatext--vb-and-c.md)             | Proporciona propiedades para obtener información sobre atributos de metadatos textuales complejos.                                                                            |
| [IWMPNetwork](iwmpnetwork--vb-and-c.md)                       | Proporciona propiedades y métodos para acceder a estadísticas relacionadas con la calidad de una conexión de red y para especificar y recuperar la configuración del proxy de red.     |
| **IWMPPlayerApplication**                                      | No se admite para la programación de .NET.                                                                                                                               |
| **IWMPPlayerServices**                                         | No se admite para la programación de .NET.                                                                                                                               |
| **IWMPPlayerServices2**                                        | No se admite para la programación de .NET.                                                                                                                               |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                     | Proporciona propiedades y métodos para organizar, administrar y manipular elementos multimedia en una lista de reproducción.                                                                    |
| [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md)           | Tiene acceso a una colección de [interfaces IWMPPlaylist](iwmpplaylist--vb-and-c.md) por número de índice.                                                                   |
| [IWMPPlaylistCollection](iwmpplaylistcollection--vb-and-c.md) | Proporciona métodos para manipular [interfaces IWMPPlaylist](iwmpplaylist--vb-and-c.md) [e IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md) en una colección. |
| [IWMPQuery](iwmpquery--vb-and-c.md)                           | Representa una consulta compuesta.                                                                                                                                      |
| [IWMPSettings](iwmpsettings--vb-and-c.md)                     | Proporciona propiedades y métodos que obtienen o establecen los valores de Reproductor de Windows Media configuración.                                                                      |
| [IWMPSettings2](iwmpsettings2--vb-and-c.md)                   | Proporciona propiedades y un método que complementan la **interfaz IWMPSettings.**                                                                                  |
| [IWMPStringCollection](iwmpstringcollection--vb-and-c.md)     | Proporciona una propiedad y un método para tener acceso a una colección de cadenas por número de índice.                                                                           |
| [IWMPStringCollection2](iwmpstringcollection2--vb-and-c.md)   | Proporciona métodos que complementan **la interfaz IWMPStringCollection.**                                                                                          |
| **IWMPSyncDevice**                                             | No se admite para la programación de .NET.                                                                                                                               |
| **IWMPSyncDevice2**                                            | No se admite para la programación de .NET.                                                                                                                               |
| **IWMPSyncServices**                                           | No se admite para la programación de .NET.                                                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia del modelo de objetos Visual Basic .NET y C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 




