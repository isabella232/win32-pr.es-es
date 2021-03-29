---
title: Interfaces de SDK de WMP
description: Interfaces de SDK de WMP
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
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
ms.openlocfilehash: ffff5a4c609d13d84972989ac32dae1600f5f02d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421763"
---
# <a name="wmp-sdk-interfaces"></a>Interfaces de SDK de WMP

En esta sección se documentan las interfaces COM expuestas por el control ActiveX de Windows Media Player y el control ActiveX de Windows Media Player Mobile.

Los métodos de descriptor de acceso de la interfaz **IWMPCore** o **IWMPPlayer** se usan para recuperar interfaces específicas. Estas interfaces, a su vez, pueden tener métodos de descriptor de acceso para recuperar otras interfaces. La llamada a **QueryInterface** en una de estas interfaces solo es necesaria cuando se recupera la versión base de una interfaz y se desea llamar a un método en una versión posterior de la misma interfaz.

> [!Note]  
> Todos los métodos y eventos son totalmente compatibles con Windows Media Player 10 Mobile y versiones posteriores, a menos que se indique explícitamente lo contrario.

El control Windows Media Player expone las siguientes interfaces.

| Interfaz                                                    | Descripción                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_WMPOCXEvents](-wmpocxevents-interface.md)                | Proporciona eventos que se originan en el control Media Player de Windows al que puede responder un programa de incrustación.                                                                              |
| [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | Obtiene acceso a un CD o DVD de una unidad.                                                                                                                                                          |
| [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | Proporciona métodos para administrar la creación de CDs de audio.                                                                                                                                            |
| [IWMPCdromCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | Obtiene acceso a una colección de unidades de CD o DVD.                                                                                                                                                |
| [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | Proporciona métodos para administrar las pistas de copia de un CD de audio.                                                                                                                               |
| [IWMPClosedCaption](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | Incluye leyendas con un clip multimedia.                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | Proporciona métodos adicionales de subtítulos (CC).                                                                                                                                            |
| [IWMPControls](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | Representa los controles de transporte de Windows Media Player, como reproducir, detener y pausar.                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | Proporciona métodos de control adicionales.                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | Proporciona métodos de control adicionales.                                                                                                                                                      |
| [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | Recupera punteros a otras interfaces y obtiene acceso a las características básicas del control. Esta es la interfaz raíz del modelo de objetos de Media Player de Windows.                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | Proporciona métodos básicos adicionales.                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | Proporciona métodos básicos adicionales.                                                                                                                                                         |
| [IWMPDVD](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | Obtiene acceso al menú de contenido de un DVD.                                                                                                                                                       |
| [IWMPError](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | Obtiene acceso a una colección de punteros [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem) .                                                                                                                     |
| [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | Proporciona información sobre los errores.                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | Proporciona métodos de elemento de error adicionales.                                                                                                                                                   |
| [IWMPEvents](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | Expone eventos que se originan en el control Media Player de Windows al que puede responder un programa de incrustación.                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | Expone eventos que se originan en el control Media Player 10 de Windows al que puede responder un programa de incrustación. Estos eventos se usan específicamente para los programas de sincronización de dispositivos. |
| [IWMPEvents3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | Proporciona eventos relacionados con la copia de CD, la grabación de CD, la supervisión de carpetas y los servicios de biblioteca remota.                                                                                        |
| [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | Proporciona métodos para enumerar, examinar y modificar las carpetas de archivos que Windows Media Player supervisa para el contenido multimedia digital.                                                                |
| [IWMPGraphCreation](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | Administra el gráfico de DirectShow.                                                                                                                                                             |
| [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)                               | Representa una biblioteca.                                                                                                                                                                     |
| [IWMPLibraryServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)               | Proporciona métodos para enumerar las bibliotecas.                                                                                                                                                  |
| [IWMPLibrarySharingServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices) | Proporciona métodos para administrar el uso compartido de bibliotecas.                                                                                                                                               |
| [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                   | Establece y recupera las propiedades de un elemento multimedia.                                                                                                                                        |
| [IWMPMedia2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia2)                                 | Proporciona métodos adicionales para establecer y recuperar las propiedades de un elemento multimedia.                                                                                                           |
| [IWMPMedia3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3)                                 | Proporciona métodos adicionales para establecer y recuperar las propiedades de un elemento multimedia.                                                                                                           |
| [IWMPMediaCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)               | Obtiene acceso a una colección de punteros [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) .                                                                                                                             |
| [IWMPMediaCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)             | Proporciona métodos que complementan la interfaz **IWMPMediaCollection** .                                                                                                                   |
| [IWMPMetadataPicture](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture)               | Recupera información sobre el atributo de metadatos de **WM/imagen** .                                                                                                                        |
| [IWMPMetadataText](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext)                     | Recupera información sobre los atributos de metadatos de texto complejos.                                                                                                                          |
| [IWMPNetwork](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpnetwork)                               | Establece y recupera las propiedades de la conexión de red que usa Windows Media Player.                                                                                                 |
| [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | Controla el comportamiento de la interfaz de usuario del control de Media Player de Windows.                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | Proporciona métodos adicionales para controlar Media Player de Windows.                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | Proporciona métodos adicionales para controlar Media Player de Windows.                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | Proporciona métodos adicionales para controlar Media Player de Windows.                                                                                                                         |
| [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | Cambia entre un control de Windows Media Player remoto y el modo completo del reproductor. Diseñado para su uso por parte de programas de C++ que incrustan el control en modo remoto.                          |
| [IWMPPlayerServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | Lo usa el host de un control remoto para manipular el modo completo de Windows Media Player. Diseñado para su uso con C++.                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | Establece la prioridad de procesamiento en segundo plano.                                                                                                                                                  |
| [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | Crea y administra listas de reproducción.                                                                                                                                                            |
| [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | Obtiene acceso a una colección de punteros [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) por número de índice.                                                                                                       |
| [IWMPPlaylistCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | Manipula los punteros [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) y [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray) .                                                                                     |
| [IWMPQuery](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | Representa una consulta compuesta.                                                                                                                                                              |
| [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | Proporciona servicios a Windows Media Player desde un programa que hospeda el control Player. Diseñado para su uso con C++.                                                                        |
| [IWMPRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | Proporciona métodos para especificar o recuperar un valor que indica si la reproducción se produce solo en el proceso actual.                                                                          |
| [IWMPSettings](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | Establece o recupera la configuración de Media Player de Windows.                                                                                                                                          |
| [IWMPSettings2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | Establece o recupera la configuración de Media Player de Windows.                                                                                                                                          |
| [IWMPSkinManager](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | Especifica la máscara usada con Media Player de Windows.                                                                                                                                        |
| [IWMPStringCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | Obtiene acceso a una colección de cadenas.                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | Proporciona métodos que complementan la interfaz **IWMPStringCollection** .                                                                                                                  |
| [IWMPSyncDevice](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | Representa un dispositivo que puede sincronizar archivos multimedia digitales con Windows Media Player 10.                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | Proporciona un método que complementa la interfaz **IWMPSyncDevice** .                                                                                                                      |
| [IWMPSyncServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | Enumera los dispositivos disponibles que pueden sincronizar archivos multimedia digitales con Windows Media Player 10.                                                                                       |
| [IWMPTranscodePolicy](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | Proporciona un método implementado por los filtros de origen de DirectShow para administrar el cambio del formato de los archivos multimedia digitales.                                                                          |
| [IWMPVideoRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | Proporciona un método que configura el representador de vídeo mejorado que usa Windows Media Player.                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia del modelo de objetos para C++**](object-model-reference-for-c.md)
</dt> </dl>

 

 




