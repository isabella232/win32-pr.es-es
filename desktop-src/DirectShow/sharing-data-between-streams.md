---
description: Compartir datos entre secuencias
ms.assetid: e18eecf8-9475-420a-9a60-4b1b5f8fd43a
title: Compartir datos entre secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0b2f53fe1952bbc16711f7c7e39c3182ba94a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495233"
---
# <a name="sharing-data-between-streams"></a>Compartir datos entre secuencias

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.

 

El procesamiento de datos multimedia normalmente requiere una gran cantidad de recursos del sistema; por lo tanto, debe evitar copiar los datos siempre que sea posible. La arquitectura de streaming admite ejemplos de secuencias compartidas, un mecanismo que mueve datos de un flujo a otro sin copiarlos. Este búfer permite el transporte eficaz de datos entre dos flujos aunque el flujo de destino no admita específicamente el formato de datos subyacente.

Por ejemplo, suponga que tiene una secuencia multimedia con tres flujos de datos: vídeo y audio, y marca de tiempo de datos URL para que coincida con el contenido de vídeo. Quiere escribir una aplicación que agregue un aviso de propiedad intelectual en cada fotograma de vídeo y escriba los datos en otra secuencia para el almacenamiento, pero la aplicación no entiende ningún formato de datos, excepto el flujo de vídeo. En el flujo de vídeo, se crea un ejemplo asociado a la superficie DirectDraw deseada. Después, puede crear un flujo de salida llamando al método [**IDirectDrawMediaStream:: CreateSample**](/previous-versions/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-createsample) con ese puntero a la misma superficie o [**IMediaStream:: CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample). En ambos casos, los flujos de entrada y salida comparten la superficie DirectDraw. Dado que entiende el formato de vídeo, puede tener acceso a esta superficie según sea necesario.

Para recuperar los otros punteros de secuencia de origen (audio y URL), enumere el flujo de contenedor de origen y los punteros a las secuencias de no vídeo. Cada uno de estos flujos de origen tiene un flujo de salida asociado en el contenedor de flujos de salida. Recupere estos punteros de salida llamando al método [**IMultiMediaStream:: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) en el contenedor de salida con cada uno de los punteros de flujo de origen. En los pasos siguientes se describe este proceso.

1.  Llame a [**IMultiMediaStream:: EnumMediaStreams**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-enummediastreams) para recuperar un puntero a una secuencia de origen. Asegúrese de que no es el flujo de vídeo, ya que la aplicación ya entiende su formato.
2.  Llame a [**IMultiMediaStream:: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) en la secuencia de contenedor de salida con el puntero del paso 1. Esto devuelve un puntero al flujo de salida deseado.
3.  Llame a [**AllocateSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-allocatesample) en el flujo de origen.
4.  Llame a [**CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) en el flujo de salida.
5.  Llame a [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) en el flujo de origen para leer los datos.
6.  Llame a [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) en el flujo de salida para escribir los datos.

Repita estos pasos para cada flujo cuyo formato no admita. Cuando ambos ejemplos terminen de actualizarse, el flujo de salida tendrá todos los datos de la secuencia de origen y se hará.

 

 



