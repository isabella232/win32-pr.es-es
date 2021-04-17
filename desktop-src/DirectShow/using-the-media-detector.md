---
description: Uso del detector de medios
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Uso del detector de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebdb05eb47c7efabcc3234fb6ac2411a46e40d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678625"
---
# <a name="using-the-media-detector"></a>Uso del detector de medios

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

El detector de medios es un objeto auxiliar que puede recuperar información sobre un archivo, como el número de flujos, su tipo y su duración. También contiene métodos para recuperar fotogramas de póster de un flujo de vídeo. Expone la interfaz [**IMediaDet**](imediadet.md) .

El detector de medios funciona en uno de dos modos. Cuando se crea una instancia del detector de medios, no se adjunta a un archivo de origen determinado. En este modo, puede recuperar la información de la secuencia de varios archivos de código fuente. Sin embargo, una vez que use el detector de medios para obtener un fotograma de póster, cambia al *modo de agarre de mapa de bits*. En el modo de captura de mapa de bits, el detector de medios se adjunta a una secuencia de vídeo específica y los métodos de información de la secuencia ya no funcionan. Además, no hay forma de volver a cambiar el detector de medios a su modo de inicio. Por lo tanto, obtenga cualquier información de flujo que necesite antes de recuperar fotogramas de póster, o bien cree nuevas instancias del detector de medios para cada flujo.

Para obtener información de la secuencia, haga lo siguiente:

1.  Llame a [**IMediaDet::p \_ nombre**](imediadet-put-filename.md) de archivo UT con el nombre del archivo de código fuente.
2.  Llame a [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) para obtener el número de flujos en el origen.
3.  Especifique un número de secuencia con [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md). A continuación, llame a uno o varios de los métodos siguientes:
    -   [**IMediaDet:: get \_ StreamType**](imediadet-get-streamtype.md): recupera el tipo de archivo multimedia de la secuencia.
    -   [**IMediaDet:: get \_ StreamLength**](imediadet-get-streamlength.md): recupera la duración de la secuencia.
    -   [**IMediaDet:: get \_ Velocidad de**](imediadet-get-framerate.md)fotogramas: recupera la velocidad de fotogramas de un flujo de vídeo.

Para obtener un fotograma de póster, especifique el número de secuencia, como en el paso anterior. Después, llame a [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md), que copia un fotograma de póster en un búfer o [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md), que guarda un fotograma de póster en un archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con orígenes](working-with-sources.md)
</dt> </dl>

 

 



