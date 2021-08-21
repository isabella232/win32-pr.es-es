---
description: Uso compartido de datos entre Secuencias
ms.assetid: e18eecf8-9475-420a-9a60-4b1b5f8fd43a
title: Uso compartido de datos entre Secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4137d56a9d90f524ee2e5c67b6a4d726d9478e824513d0fe7879c95ce094af1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072569"
---
# <a name="sharing-data-between-streams"></a>Uso compartido de datos entre Secuencias

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow gráfico de filtros.

 

El procesamiento de datos multimedia normalmente requiere una gran cantidad de recursos del sistema; por lo tanto, debe evitar copiar datos siempre que sea posible. La arquitectura de streaming admite ejemplos de flujos compartidos, un mecanismo que mueve los datos de una secuencia a otra sin copiarlos. Este búfer permite el transporte eficaz de datos entre dos secuencias incluso si el flujo de destino no admite específicamente el formato de datos subyacente.

Por ejemplo, suponga que tiene una secuencia multimedia con tres flujos de datos: vídeo y audio, y datos de dirección URL con marca de tiempo para que coincidan con el contenido del vídeo. Quiere escribir una aplicación que agrega un aviso de copyright en cada fotograma de vídeo y escribe los datos en otra secuencia para su almacenamiento, pero la aplicación no entiende ningún formato de datos, excepto la secuencia de vídeo. Para la secuencia de vídeo, cree un ejemplo asociado a la superficie de DirectDraw deseada. A continuación, puede crear un flujo de salida llamando al método [**IDirectDrawMediaStream::CreateSample**](/previous-versions/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-createsample) con ese puntero a la misma superficie o a [**IMediaStream::CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample). En ambos casos, los flujos de entrada y salida comparten la superficie de DirectDraw. Dado que comprende el formato de vídeo, puede acceder a esta superficie según sea necesario.

Para recuperar los demás punteros de flujo de origen (audio y dirección URL), enumere la secuencia del contenedor de origen y tome punteros a las secuencias que no son de vídeo. Cada uno de estos flujos de origen tiene un flujo de salida asociado en el contenedor de flujo de salida. Recupere estos punteros de salida llamando al método [**IMultiMediaStream::GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) en el contenedor de salida con cada uno de los punteros de flujo de origen. En los pasos siguientes se describe este proceso.

1.  Llame [**a IMultiMediaStream::EnumMediaStreams**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-enummediastreams) para recuperar un puntero a una secuencia de origen. Asegúrese de que no es la secuencia de vídeo, porque la aplicación ya entiende su formato.
2.  Llame [**a IMultiMediaStream::GetMediaStream en**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) el flujo de contenedor de salida con el puntero del paso 1. Esto devuelve un puntero al flujo de salida deseado.
3.  Llame [**a AllocateSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-allocatesample) en la secuencia de origen.
4.  Llame [**a CreateSharedSample en**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) el flujo de salida.
5.  Llame [**a Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) en el flujo de origen para leer los datos.
6.  Llame [**a Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) en el flujo de salida para escribir los datos.

Repita estos pasos para cada secuencia cuyo formato no admita. Cuando ambos ejemplos terminen de actualizarse, el flujo de salida tiene todos los datos del flujo de origen y ya está listo.

 

 



