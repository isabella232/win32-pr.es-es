---
title: Uso de la conmutación de streaming de eventos en vivo
description: Uso de la conmutación de streaming de eventos en vivo
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
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
- Reproductor de Windows Media, cambio de secuencia de eventos en directo
- Reproductor de Windows Media, conmutación de flujo de eventos
- Reproductor de Windows Media,inserción de ad
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
ms.openlocfilehash: d8524fe1a83a6b3276c274726fa27fa7fcccb97b88f0384a54e5433d09380501
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134368"
---
# <a name="using-live-event-stream-switching"></a>Uso de la conmutación de streaming de eventos en vivo

Los medios de streaming también se pueden controlar mediante la interacción de comandos de script insertados en una secuencia de medios con Windows de metarchivo multimedia en una lista de reproducción de metarchivo.

Un evento es un tipo determinado de comando de script insertado en una secuencia de medios o un archivo multimedia. Cuando el Reproductor de Windows Media recibe el comando de script, procesa el evento tal como lo define el elemento **EVENT** en la lista de reproducción de metarchivo. Reproductor de Windows Media cambia de la secuencia actual que está representando y representa el contenido al que se hace referencia en el elemento EVENT de la lista de reproducción **de** metarchivo. El **elemento EVENT** se usa normalmente en producción en vivo.

Un **elemento EVENT** es similar a un elemento **ENTRY,** pero cada uno controla la reproducción de secuencias y archivos multimedia de forma diferente. El **elemento ENTRY** se usa para crear listas de reproducción. Una secuencia o un archivo multimedia al que se hace referencia en un **elemento ENTRY** comienza a reproducirse cuando finaliza la secuencia o el archivo multimedia al que se hace referencia en **la entrada** anterior. Una secuencia a la que se hace referencia en **un evento** solo se reproduce cuando se recibe un comando de script específico. Por ejemplo, cuando Reproductor de Windows Media un comando de script con la cadena de tipo "EVENT" y la cadena de comandos "Adlink", busca en la lista de reproducción los siguientes elementos.


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



Reproductor de Windows Media a continuación, cambia de la secuencia en vivo para reproducir la secuencia o el archivo multimedia contenido en **event**, en este caso Adlink.wma. El código `WHENDONE="RESUME"` indica a Reproductor de Windows Media que reanude la reproducción de la secuencia anterior cuando adlink.wma haya finalizado.

> [!Note]  
> Si no se controlan todos los eventos insertados en un flujo multimedia o un archivo multimedia, se pueden producir resultados inesperados.

 

Si desea usar el cambio de secuencia de eventos en directo, debe incluir un elemento **EVENT** en la lista de reproducción para controlar cada comando de script de eventos insertado en los flujos multimedia o archivos multimedia de la lista de reproducción. Antes de crear la lista de reproducción, debe conocer los detalles sobre qué comandos de script se insertan en el contenido multimedia digital. Si hay un comando de script de eventos que Reproductor de Windows Media omitir, incluya un elemento **EVENT** en la lista de reproducción para controlar el evento, pero haga referencia a una dirección URL ficticia en el controlador de eventos.

## <a name="ad-insertion"></a>Inserción de anuncios

Esta técnica se puede usar para la inserción de anuncios. Por ejemplo, durante una difusión en vivo por Internet de un juego de bola, se puede enviar un comando al principio de cada pausa comercial que indique a cada cliente (Reproductor de Windows Media) que reproduta los anuncios que aparecen en su lista de reproducción. Cuando los clientes terminan de reproducir los anuncios, la lista de reproducción indica a cada cliente que se reduzca a la difusión en directo. El **contenido multimedia EVENT** solo se representará cuando el medio de streaming al que se tiene acceso difusione scripts insertados con el nombre **EVENT** correspondiente.

Las posibilidades  inherentes a la conmutación de EVENTOS se aprecian mejor al contrastar cómo los anuncios llegan a los espectadores a través de la difusión estándar y por vía aérea con la forma en que los anuncios pueden llegar a los espectadores mediante Windows Media Technologies. Históricamente, los anuncios de difusión solo se podían dirigir aproximadamente a los espectadores, usando los datos de clasificaciones como criterio principal. Los anuncios enviados mediante Windows Media Technologies se pueden dirigir directamente al usuario de destino, ya que los **EVENT** y las listas de reproducción se pueden crear sobre la marcha en función de la entrada del usuario. Para obtener más información, vea [Personalizing Media Delivery](personalizing-media-delivery.md).

También puede usar listas de reproducción de metarchivo para mostrar gráficos, audio y texto personalizados para publicidad. Puede usar el elemento **BANNER como** elemento secundario de **un evento** para mostrar un gráfico de mensaje de publicidad. El **elemento BANNER** proporciona la ruta de acceso y el archivo que contiene los gráficos del banner de publicidad. También puede proporcionar un vínculo a un sitio o archivo mediante el **elemento secundario MOREINFO.** La dirección URL del **elemento MOREINFO** puede proporcionar un vínculo a incluso más anuncios en la Web. En el ejemplo siguiente se muestra el uso de estos elementos.

Código de ejemplo


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



En el ejemplo siguiente se inserta ad Favor.wma en la secuencia de unidifusión de difusión BallGame cuando un cliente recibe un comando de script **EVENT** con el atributo **NAME** establecido en "Time-Out". **CLIENTSKIP se** establece en NO para evitar que se opa el anuncio transmitido. En este ejemplo, el anuncio transmitido debe reproducirse antes de volver a la secuencia original. Una vez finalizado el anuncio, el cliente reanuda la reproducción de la secuencia original.

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

[**Listas de reproducción de metarchivo**](metafile-playlists.md)
</dt> <dt>

[**Uso de listas de reproducción de metarchivo**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




