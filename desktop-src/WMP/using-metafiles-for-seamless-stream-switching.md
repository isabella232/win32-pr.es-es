---
title: Uso de metarchivos para la conmutación de secuencias sin problemas
description: Uso de metarchivos para la conmutación de secuencias sin problemas
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
keywords:
- Windows Listas de reproducción de metarchivos multimedia, cambio de secuencia de eventos en vivo
- playlists,live event stream switching
- listas de reproducción de metarchivo, cambio de secuencia de eventos en vivo
- Windows Listas de reproducción de metarchivo multimedia, conmutación de secuencias de eventos
- playlists,event stream switching
- listas de reproducción de metarchivo, conmutación de flujo de eventos
- Windows Listas de reproducción de metarchivo multimedia, inserción de anuncios
- listas de reproducción, inserción de ad
- listas de reproducción de metarchivo, inserción de ad
- Reproductor de Windows Media, cambio de secuencia de eventos en vivo
- Reproductor de Windows Media, conmutación de flujo de eventos
- Reproductor de Windows Media,ad inserción
- cambio de streaming de eventos en directo
- conmutación del flujo de eventos
- inserción de anuncios
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361727"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a>Uso de metarchivos para la conmutación de secuencias sin problemas

Puede facilitar el cambio de flujo sin problemas mediante listas de reproducción de metarchivo. Normalmente, cuando finaliza un fragmento de contenido, se produce el almacenamiento en búfer para el siguiente clip o secuencia antes de que se abra (si es contenido recibido de un servidor multimedia de streaming). Microsoft Servicios de Windows Media permite eliminar, o al menos minimizar, este tiempo de almacenamiento en búfer y hacer que otro fragmento de contenido transmitido comience a reproducirse casi inmediatamente. El modo normal de funcionamiento de Reproductor de Windows Media es abrir la siguiente secuencia multimedia a la que hace referencia la lista de reproducción 20 segundos antes del final de la secuencia que se representa actualmente. Por lo general, esto proporciona una transición sin problemas entre secuencias multimedia, en función de otros factores, como los tiempos de acceso web.

Use el **elemento EVENT** de una lista de reproducción junto con los comandos OPENEVENT del codificador para facilitar el cambio sin problemas entre secuencias o archivos. El envío de un comando OPENEVENT 20 segundos o más antes del comando EVENT puede minimizar los retrasos en el cambio de secuencia. A Reproductor de Windows Media puede cargar previamente una parte del próximo contenido de streaming en un búfer.

Use Windows Media Encoder para enviar un comando de script en la secuencia con el formato siguiente:


```XML
OPENEVENT eventname 

```



El nombre del evento debe ser el definido en el elemento **EVENT** de la lista de reproducción. Cuando Reproductor de Windows Media un comando de script OPENEVENT del codificador, busca el elemento **EVENT** en la lista de reproducción y comienza a almacenar en búfer el clip o secuencia definido en el **elemento EVENT.** Reproductor de Windows Media contiene esta información hasta el evento real del mismo nombre. Cuando se recibe el evento con nombre, Reproductor de Windows Media cambia a ese contenido almacenado previamente en búfer.

> [!Note]  
> No se pueden usar caracteres Unicode para el comando de script OPENEVENT en el archivo multimedia o el **elemento EVENT** de la lista de reproducción.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación de listas de reproducción de metarchivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Listas de reproducción de metarchivo**](metafile-playlists.md)
</dt> <dt>

[**Evento Player.ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Uso de listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




