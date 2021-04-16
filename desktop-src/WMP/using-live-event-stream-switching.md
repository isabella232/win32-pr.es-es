---
title: Usar el cambio de secuencia de eventos en directo
description: Usar el cambio de secuencia de eventos en directo
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
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
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268481"
---
# <a name="using-live-event-stream-switching"></a>Usar el cambio de secuencia de eventos en directo

Los archivos multimedia de streaming también se pueden controlar mediante la interacción de los comandos de script insertados en una secuencia de medios con elementos de metarchivo de Windows Media en una lista de reproducción de metarchivo.

Un evento es un tipo determinado de comando de script incrustado en una secuencia de medios o un archivo multimedia. Cuando el control de Media Player de Windows recibe el comando de script, procesa el evento tal y como lo define el elemento de **evento** en la lista de reproducción del metarchivo. Windows Media Player cambia del flujo actual que se está representando y representa el contenido al que se hace referencia en el elemento de **evento** de lista de reproducción de metarchivo. El elemento de **evento** se utiliza normalmente en producción en vivo.

Un elemento de **evento** tiene un aspecto similar a un elemento de **entrada** , pero cada uno de ellos controla la reproducción de secuencias y archivos multimedia de manera diferente. El elemento **entry** se usa para crear listas de reproducción. Un flujo o un archivo multimedia al que se hace referencia en un elemento de **entrada** comienza A reproducirse cuando finaliza la secuencia o el archivo multimedia al que se hace referencia en la **entrada** anterior. Un flujo al que se hace referencia en un **evento** solo se reproduce cuando se recibe un comando de script específico. Por ejemplo, cuando Windows Media Player recibe un comando de script con la cadena de tipo "EVENT" y la cadena de comando "Adlink", busca los siguientes elementos en la lista de reproducción.


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



Windows Media Player, a continuación, cambia de la secuencia en directo para reproducir la secuencia o el archivo multimedia contenidos en el **evento**, en este caso Adlink. WMA. El código `WHENDONE="RESUME"` indica a Windows Media Player que reanude la reproducción de la secuencia anterior cuando Adlink. WMA ha finalizado.

> [!Note]  
> Si no se controla cada evento incrustado en una secuencia de medios o en un archivo multimedia, pueden producirse resultados inesperados.

 

Si desea usar el cambio de secuencia de eventos en directo, debe incluir un elemento de **evento** en la lista de reproducción para controlar cada comando de script de eventos incrustado en los flujos multimedia o archivos multimedia de la lista de reproducción. Antes de crear la lista de reproducción, debe conocer los detalles sobre qué comandos de script están incrustados en el contenido multimedia digital. Si hay un comando de script de eventos que desea que Windows Media Player omita, incluya un elemento de **evento** en la lista de reproducción para controlar el evento, pero haga referencia a una dirección URL ficticia en el controlador de eventos.

## <a name="ad-insertion"></a>Inserción de anuncio

Esta técnica se puede usar para la inserción de anuncios. Por ejemplo, durante una difusión en Internet en directo de un juego de bola, se puede enviar un comando al principio de cada interrupción comercial que indique a cada cliente (Windows Media Player) que juegue los comerciales que aparecen en su lista de reproducción. Cuando los clientes finalizan la reproducción de los comerciales, la lista de reproducción indica a cada cliente que vuelva a la difusión en directo. El contenido de los medios de **evento** solo se representará cuando el medio de streaming al que se tiene acceso difunde scripting incrustado con el nombre de **evento** correspondiente.

Las posibilidades inherentes al cambio de **eventos** se aprecian mejor al contrastar el modo en que los anuncios llegan a los visores a través de la difusión estándar y por aire con el modo en que los anuncios pueden llegar a los visores mediante tecnologías de Windows Media. Históricamente, los anuncios de difusión solo podían estar dirigidos aproximadamente a visores, con los datos de clasificación como criterio principal. Los anuncios enviados mediante tecnologías de Windows Media pueden estar dirigidos directamente al usuario de destino, ya que los **eventos** y las listas de reproducción se pueden crear sobre la marcha en función de los datos proporcionados por el usuario. Para obtener más información, consulte [Personalización de la entrega de contenido multimedia](personalizing-media-delivery.md).

También puede utilizar listas de reproducción de metarchivos para mostrar gráficos, audio y texto personalizados para publicidad. Puede usar el elemento **banner** como un elemento secundario de un **evento** para mostrar un gráfico de mensaje de anuncio. El elemento **banner** proporciona la ruta de acceso y el archivo que contiene los gráficos de la pancarta de publicidad. También puede proporcionar un vínculo a un sitio o archivo mediante el elemento secundario **MOREINFO** . La dirección URL en el elemento **MOREINFO** puede proporcionar un vínculo a incluso más anuncios en la Web. En el siguiente ejemplo se muestra el uso de estos elementos.

Código de ejemplo


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



En el ejemplo siguiente se inserta ad Advert. WMA en el flujo de unidifusión de difusión BallGame cuando un cliente recibe un **evento** de comando de script con el atributo de **nombre** establecido en "tiempo de espera". **CLIENTSKIP** está establecido en no para evitar que se omita el anuncio transmitido. En este ejemplo, el anuncio transmitido por secuencias debe reproducirse antes de volver a la secuencia original. Cuando finaliza el anuncio, el cliente reanuda la reproducción de la secuencia original.

Código de ejemplo


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Usar listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




