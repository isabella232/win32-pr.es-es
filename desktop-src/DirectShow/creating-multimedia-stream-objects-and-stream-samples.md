---
description: Creación de objetos de secuencia multimedia y ejemplos de secuencia
ms.assetid: 1aecdd39-f1b3-490b-b092-86d51439be02
title: Creación de objetos de secuencia multimedia y ejemplos de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cab467a67663cf1fa99df8d887b522f8971e24b97d4b99dd148f329fc3c7d45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054795"
---
# <a name="creating-multimedia-stream-objects-and-stream-samples"></a>Creación de objetos de secuencia multimedia y ejemplos de secuencia

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow gráfico de filtros.

 

Los objetos que admiten [**la interfaz IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) son los contenedores básicos para los flujos de datos multimedia. La **interfaz IMultiMediaStream** incluye métodos que enumeran los flujos de datos del objeto. Estas secuencias suelen ser datos de audio y vídeo, pero pueden incluir datos de cualquier formato, como subtítulos, texto sin formato o código de tiempo SMPTE. Sin embargo, la interfaz **IMultiMediaStream** es un contenedor genérico; Los desarrolladores pueden crear otras versiones de la interfaz que admitan formatos de datos específicos. Los objetos que implementan [**la interfaz IAMMultiMediaStream,**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) por ejemplo, pueden enumerar y controlar secuencias de cualquier DirectShow formato de datos. Dado que los flujos de datos individuales son específicos del formato, admiten al menos dos interfaces diferentes: una genérica y otra específica de datos. Cada secuencia admite la [**interfaz IMediaStream,**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) que proporciona métodos para recuperar su formato y un puntero a la propia secuencia. Por otro lado, la interfaz [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) tiene métodos que se tratan específicamente con la representación de datos de vídeo. Cualquier interfaz derivada de **IMultiMediaStream** también admite la creación de ejemplos de secuencias, las unidades básicas de datos de streaming.

Un ejemplo multimedia es una referencia a un objeto que contiene los datos multimedia. Para una imagen de vídeo, se trata de una superficie de DirectDraw. El contenido exacto del ejemplo varía en función del tipo de medio (sonido, texto, entre otros). Dado que un ejemplo es solo una referencia al objeto de datos, cualquier número de muestras de secuencia puede hacer referencia al mismo objeto. La [**interfaz IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) proporciona métodos que obtienen y establecen las características de un ejemplo, como la hora de inicio y de detección, el estado y la asociación de secuencias. El [**método IStreamSample::Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) actualiza los datos del ejemplo en el caso de secuencias legibles. En el caso de las secuencias grabables, escribirá los datos del ejemplo en la secuencia. Normalmente, se usa el **método Update** en un bucle que representa, transfiere o almacena datos de streaming.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la arquitectura de streaming multimedia](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



