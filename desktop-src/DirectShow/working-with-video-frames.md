---
description: Trabajar con fotogramas de vídeo
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Trabajar con fotogramas de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687720"
---
# <a name="working-with-video-frames"></a>Trabajar con fotogramas de vídeo

El vídeo sin comprimir es una secuencia de mapas de bits que se reproducen en una sucesión rápida, normalmente a una velocidad de aproximadamente 30 fotogramas por segundo. Dado que la mayoría del vídeo entra en un gráfico de filtros de DirectShow en formato comprimido, el flujo de vídeo suele pasar por un descodificador para la descompresión. Muchos descodificadores generan datos en formato YUV y dejan la conversión final a RGB para el hardware de vídeo justo antes de la representación. Si un descodificador usa la aceleración de vídeo de DirectX, el hardware de vídeo realiza el trabajo adicional para descodificar la imagen. Por lo tanto, es posible que no se realice la descompresión final de los mapas de bits hasta que los datos lleguen al hardware de vídeo.

Pero para realizar muchos tipos de análisis, procesamiento o edición de vídeo, a menudo es necesario trabajar en mapas de bits sin comprimir en algún tipo de formato RGB o YUV antes de que se representen o se escriban en el archivo. Este trabajo se realiza normalmente en un filtro de transformación basado en la clase base [**CTransformFilter**](ctransformfilter.md) , específicamente en el método **Transform** . Este método recibe un puntero a un objeto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) que encapsula los datos de vídeo. El método **IMediaSample:: GetPointer** devuelve un puntero al primer byte de los datos sin procesar. En el caso de los marcos sin comprimir, estos datos se componen de píxeles a los que el filtro puede tener acceso o modificar directamente. En las secciones siguientes se proporciona información general que le ayudará a trabajar de forma eficaz con los datos DIB de esta manera.

> [!Note]  
> También puede modificar los bits mediante las funciones GDI, GDI+, DirectDraw o Direct3D, pero estas técnicas quedan fuera del ámbito de este artículo.

 

Esta sección contiene los siguientes temas:

-   [De arriba abajo y Bottom-Up DIB](top-down-vs--bottom-up-dibs.md)
-   [Trabajar con RGB de 16 bits](working-with-16-bit-rgb.md)

 

 



