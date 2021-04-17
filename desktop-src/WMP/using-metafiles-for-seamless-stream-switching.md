---
title: Usar metaarchivos para la conmutación de flujos sin problemas
description: Usar metaarchivos para la conmutación de flujos sin problemas
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Listas de reproducción de metarchivos de Windows Media, conmutación de flujos de eventos en directo
- listas de reproducción, conmutación de flujos de eventos en directo
- listas de reproducción de metarchivos, conmutación de flujos de eventos en directo
- Listas de reproducción de metarchivos de Windows Media, conmutación de flujos de eventos
- listas de reproducción, conmutación de flujos de eventos
- listas de reproducción de metarchivos, conmutación de flujos de eventos
- Listas de reproducción de metarchivos de Windows Media, inserción de anuncios
- listas de reproducción, inserción de anuncios
- listas de reproducción de metarchivos, inserción de anuncios
- Windows Media Player, conmutación por secuencias de eventos en directo
- Windows Media Player, conmutación de flujos de eventos
- Windows Media Player, inserción de anuncios
- cambio de secuencia de eventos en directo
- conmutación de flujos de eventos
- inserción de anuncio
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704593"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a>Usar metaarchivos para la conmutación de flujos sin problemas

Puede facilitar el intercambio de flujos sin problemas mediante listas de reproducción de metarchivo. Normalmente, cuando un fragmento de contenido finaliza, el almacenamiento en búfer se produce para el siguiente clip o secuencia antes de que se abra (si se trata de contenido recibido de un servidor de streaming multimedia). Microsoft Windows Media Services permite eliminar, o al menos minimizar, este tiempo de almacenamiento en búfer y hacer que otro fragmento de contenido transmitido empiece a reproducirse casi de inmediato. El modo normal de funcionamiento de Windows Media Player es abrir la siguiente secuencia de medios a la que hace referencia la lista de reproducción 20 segundos antes del final del flujo representado actualmente. Por lo general, esto proporciona una transición sin problemas entre flujos multimedia, en función de otros factores, como los tiempos de acceso web.

Use el elemento **Event** en una lista de reproducción junto con los comandos OPENEVENT del codificador para facilitar el cambio sin problemas entre las secuencias o los archivos. El envío de un comando OPENEVENT de 20 segundos o más antes del comando de evento puede minimizar los retrasos en el cambio de secuencia. A continuación, Windows Media Player puede cargar previamente una parte del próximo contenido de streaming en un búfer.

Use el codificador de Windows Media para enviar un comando de script en la secuencia con el siguiente formato:


```XML
OPENEVENT eventname 

```



El nombre del evento debe ser el que se haya definido en el elemento de **evento** de la lista de reproducción. Cuando Windows Media Player recibe un comando de script de OPENEVENT desde el codificador, busca el elemento de **evento** en la lista de reproducción y comienza a almacenar en búfer el clip o el flujo definido en el elemento de **evento** . Windows Media Player contiene esta información hasta el evento real del mismo nombre. Cuando se recibe el evento con nombre, Windows Media Player cambia a ese contenido almacenado previamente en el búfer.

> [!Note]  
> No se pueden usar caracteres Unicode para el comando de script OPENEVENT en el archivo multimedia o en el elemento de **evento** de la lista de reproducción.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Crear listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Evento Player. comando**](player-player-scriptcommand.md)
</dt> <dt>

[**Usar listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




