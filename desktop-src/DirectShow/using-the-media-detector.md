---
description: Uso del detector de medios
ms.assetid: 462150d5-7315-4c2b-81b0-964a788ec47d
title: Uso del detector de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22294a25dd6254cd310f0a77a7004c597c857a36d8865ad4757cb404fc114f00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086685"
---
# <a name="using-the-media-detector"></a>Uso del detector de medios

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

El detector de medios es un objeto auxiliar que puede recuperar información sobre un archivo, como el número de secuencias, su tipo y su duración. También contiene métodos para recuperar fotogramas de póster de una secuencia de vídeo. Expone la [**interfaz IMediaDet.**](imediadet.md)

El detector de medios funciona en uno de estos dos modos. Cuando se crea una instancia del detector de medios, no se adjunta a un archivo de código fuente determinado. En este modo, puede recuperar información de secuencia de varios archivos de origen. Sin embargo, una vez que se usa el detector de medios para obtener un marco de póster, cambia al modo *de captura de mapa de bits*. En el modo de captura de mapa de bits, el detector de medios está asociado a una secuencia de vídeo específica y los métodos de información de secuencia ya no funcionan. Además, no hay ninguna manera de volver a cambiar el detector de medios a su modo de inicio. Por lo tanto, obtenga cualquier información de secuencia que necesite antes de recuperar fotogramas de póster o cree nuevas instancias del detector de medios para cada secuencia.

Para obtener información de flujo, haga lo siguiente:

1.  Llame [**a IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) con el nombre del archivo de origen.
2.  Llame [**a IMediaDet::get \_ OutputStreams**](imediadet-get-outputstreams.md) para obtener el número de secuencias en el origen.
3.  Especifique un número de secuencia [**con IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md). A continuación, llame a uno o varios de los métodos siguientes:
    -   [**IMediaDet::get \_ StreamType:**](imediadet-get-streamtype.md)recupera el tipo de medio de la secuencia.
    -   [**IMediaDet::get \_ StreamLength:**](imediadet-get-streamlength.md)recupera la duración de la secuencia.
    -   [**IMediaDet::get \_ FrameRate:**](imediadet-get-framerate.md)recupera la velocidad de fotogramas de una secuencia de vídeo.

Para obtener un marco de póster, especifique el número de secuencia, como en el paso anterior. A continuación, llame a [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md), que copia un marco de póster en un búfer, o a [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md), que guarda un marco de póster en un archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con orígenes](working-with-sources.md)
</dt> </dl>

 

 



