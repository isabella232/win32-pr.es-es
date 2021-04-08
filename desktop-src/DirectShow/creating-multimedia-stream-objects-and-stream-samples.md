---
description: Crear objetos de flujo multimedia y ejemplos de secuencias
ms.assetid: 1aecdd39-f1b3-490b-b092-86d51439be02
title: Crear objetos de flujo multimedia y ejemplos de secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cdc30129591bf1c67609ad6d15e8fd8286ae23
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003380"
---
# <a name="creating-multimedia-stream-objects-and-stream-samples"></a>Crear objetos de flujo multimedia y ejemplos de secuencias

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.

 

Los objetos que admiten la interfaz [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) son los contenedores básicos para los flujos de datos multimedia. La interfaz **IMultiMediaStream** incluye métodos que enumeran los flujos de datos del objeto; Estos flujos suelen ser datos de vídeo y audio, pero pueden incluir datos de cualquier formato, como subtítulos (CC), texto sin formato o código de tiempo SMPTE. Sin embargo, la interfaz **IMultiMediaStream** es un contenedor genérico. los desarrolladores pueden crear otras versiones de la interfaz que admiten formatos de datos específicos. Los objetos que implementan la interfaz [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) , por ejemplo, pueden enumerar y controlar las secuencias de cualquier formato de datos de DirectShow. Dado que los flujos de datos individuales tienen un formato específico, admiten al menos dos interfaces diferentes: una genérica y una específica de datos. Cada secuencia admite la interfaz [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) , que proporciona métodos para recuperar su formato y un puntero al propio flujo. La interfaz [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) , por otro lado, tiene métodos que abordan específicamente la representación de datos de vídeo. Cualquier interfaz derivada de **IMultiMediaStream** también admite la creación de ejemplos de secuencias, las unidades básicas de datos de streaming.

Un ejemplo multimedia es una referencia a un objeto que contiene los datos multimedia. En el caso de una imagen de vídeo, se trata de una superficie DirectDraw. El contenido exacto del ejemplo varía en función del tipo de medio (sonido, texto, etc.). Dado que un ejemplo es solo una referencia al objeto de datos, cualquier número de ejemplos de secuencias puede hacer referencia al mismo objeto. La interfaz [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) proporciona métodos que obtienen y establecen las características de un ejemplo, como la hora de inicio y de finalización, el estado y la Asociación de la secuencia. El método [**IStreamSample:: Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) actualiza los datos del ejemplo en el caso de las secuencias legibles. En el caso de las secuencias que se puedan escribir, escribirá los datos del ejemplo en la secuencia. Normalmente, se usa el método **Update** en un bucle que representa, transfiere o almacena datos de transmisión por secuencias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la arquitectura de streaming multimedia](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



