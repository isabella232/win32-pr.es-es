---
title: Interfaces de SDK de WMP
description: Interfaces de SDK de WMP
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
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
ms.openlocfilehash: 7db8e5ebe29e38da9f92370f60a622fad70f36395b271eb7bd86ef49f49a3d49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123505"
---
# <a name="wmp-sdk-interfaces"></a>Interfaces de SDK de WMP

En esta sección se documenta las interfaces COM expuestas por el control Reproductor de Windows Media ActiveX y el control Reproductor de Windows Media Mobile ActiveX control.

Los métodos de accessor de **la interfaz IWMPCore** **o IWMPPlayer** se usan para recuperar interfaces específicas. Estas interfaces, a su vez, pueden tener métodos de accessor para recuperar más interfaces. Llamar a **QueryInterface** en una de estas interfaces solo es necesario cuando se recupera la versión base de una interfaz y se quiere llamar a un método en una versión posterior de la misma interfaz.

> [!Note]  
> Todos los métodos y eventos son totalmente compatibles con Reproductor de Windows Media 10 Mobile y versiones posteriores, a menos que se indique explícitamente lo contrario.

El control Reproductor de Windows Media expone las interfaces siguientes.

| Interfaz                                                    | Descripción                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_WMPOCXEvents](-wmpocxevents-interface.md)                | Proporciona eventos que se origina en Reproductor de Windows Media control al que puede responder un programa de inserción.                                                                              |
| [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | Accede a un CD o DVD en una unidad.                                                                                                                                                          |
| [IWMPCdrom (IWMPCdrom )](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | Proporciona métodos para administrar la creación de CD de audio.                                                                                                                                            |
| [IWMPCdromCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | Accede a una colección de unidades de CD o DVD.                                                                                                                                                |
| [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | Proporciona métodos para administrar la copia de pistas desde un CD de audio.                                                                                                                               |
| [IWMPClosedCaption](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | Incluye subtítulos con un clip multimedia.                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | Proporciona métodos de subtítulos adicionales.                                                                                                                                            |
| [IWMPControls](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | Representa los controles de transporte de Reproductor de Windows Media, como Reproducir, Detener y Pausar.                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | Proporciona métodos de control adicionales.                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | Proporciona métodos de control adicionales.                                                                                                                                                      |
| [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | Recupera punteros a otras interfaces y accede a las características básicas del control. Esta es la interfaz raíz para el modelo Reproductor de Windows Media objeto.                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | Proporciona métodos principales adicionales.                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | Proporciona métodos principales adicionales.                                                                                                                                                         |
| [IWMPDVD](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | Accede al menú de contenido de un DVD.                                                                                                                                                       |
| [IWMPError](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | Tiene acceso a una colección [de punteros IWMPErrorItem.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                                                                                                                     |
| [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | Proporciona información sobre los errores.                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | Proporciona métodos de elemento de error adicionales.                                                                                                                                                   |
| [IWMPEvents](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | Expone eventos que se originan en el control Reproductor de Windows Media al que puede responder un programa de inserción.                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | Expone eventos que se originan en el control Reproductor de Windows Media 10 al que puede responder un programa de inserción. Estos eventos se usan específicamente para los programas de sincronización de dispositivos. |
| [IWMPEvents3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | Proporciona eventos relacionados con la limpieza de CD, la grabación de CD, la supervisión de carpetas y los servicios de biblioteca remota.                                                                                        |
| [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | Proporciona métodos para enumerar, examinar y modificar carpetas de archivos que Reproductor de Windows Media monitores de contenido multimedia digital.                                                                |
| [IWMPGraphCreation](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | Administra el DirectShow gráfico.                                                                                                                                                             |
| [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)                               | Representa una biblioteca.                                                                                                                                                                     |
| [IWMPLibraryServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)               | Proporciona métodos para enumerar bibliotecas.                                                                                                                                                  |
| [IWMPLibrarySharingServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices) | Proporciona métodos para administrar el uso compartido de bibliotecas.                                                                                                                                               |
| [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                   | Establece y recupera las propiedades de un elemento multimedia.                                                                                                                                        |
| [IWMPMedia2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia2)                                 | Proporciona métodos adicionales para establecer y recuperar las propiedades de un elemento multimedia.                                                                                                           |
| [IWMPMedia3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3)                                 | Proporciona métodos adicionales para establecer y recuperar las propiedades de un elemento multimedia.                                                                                                           |
| [IWMPMediaCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)               | Tiene acceso a una colección [de punteros IWMPMedia.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                                                                                                             |
| [IWMPMediaCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)             | Proporciona métodos que complementan **la interfaz IWMPMediaCollection.**                                                                                                                   |
| [IWMPMetadataPicture](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture)               | Recupera información sobre el atributo **de metadatos WM/Picture.**                                                                                                                        |
| [IWMPMetadataText](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext)                     | Recupera información sobre atributos de metadatos textuales complejos.                                                                                                                          |
| [IWMPNetwork](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpnetwork)                               | Establece y recupera las propiedades de la conexión de red utilizada por Reproductor de Windows Media.                                                                                                 |
| [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | Controla el comportamiento del control Reproductor de Windows Media interfaz de usuario.                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | Proporciona métodos adicionales para controlar Reproductor de Windows Media.                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | Proporciona métodos adicionales para controlar Reproductor de Windows Media.                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | Proporciona métodos adicionales para controlar Reproductor de Windows Media.                                                                                                                         |
| [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | Cambia entre un control Reproductor de Windows Media remoto y el modo completo del reproductor. Diseñado para su uso por programas de C++ que insertan el control en modo remoto.                          |
| [IWMPPlayerServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | Usado por el host de un control remoto para manipular el modo completo de Reproductor de Windows Media. Diseñado para su uso con C++.                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | Establece la prioridad de procesamiento en segundo plano.                                                                                                                                                  |
| [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | Crea y administra listas de reproducción.                                                                                                                                                            |
| [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | Tiene acceso a una colección de [punteros IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) por número de índice.                                                                                                       |
| [IWMPPlaylistCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | Manipula punteros [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) [e IWMPPlaylistArray.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                                                                                     |
| [IWMPQuery](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | Representa una consulta compuesta.                                                                                                                                                              |
| [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | Proporciona servicios para Reproductor de Windows Media desde un programa que hospeda el control Player. Diseñado para su uso con C++.                                                                        |
| [IWMPRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | Proporciona métodos para especificar o recuperar un valor que indica si la reproducción solo se produce en el proceso actual.                                                                          |
| [IWMPSettings](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | Establece o recupera Reproductor de Windows Media configuración.                                                                                                                                          |
| [IWMPSettings2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | Establece o recupera Reproductor de Windows Media configuración.                                                                                                                                          |
| [IWMPSkinManager](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | Especifica la máscara utilizada con Reproductor de Windows Media.                                                                                                                                        |
| [IWMPStringCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | Tiene acceso a una colección de cadenas.                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | Proporciona métodos que complementan **la interfaz IWMPStringCollection.**                                                                                                                  |
| [IWMPSyncDevice](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | Representa un dispositivo que puede sincronizar archivos multimedia digitales con Reproductor de Windows Media 10.                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | Proporciona un método que complementa la **interfaz IWMPSyncDevice.**                                                                                                                      |
| [IWMPSyncServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | Enumera los dispositivos disponibles que pueden sincronizar archivos multimedia digitales con Reproductor de Windows Media 10.                                                                                       |
| [IWMPTranscodePolicy](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | Proporciona un método implementado por los filtros DirectShow origen para administrar el cambio del formato de los archivos multimedia digitales.                                                                          |
| [IWMPVideoRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | Proporciona un método que configura el representador de vídeo mejorado utilizado por Reproductor de Windows Media.                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia del modelo de objetos para C++**](object-model-reference-for-c.md)
</dt> </dl>

 

 




