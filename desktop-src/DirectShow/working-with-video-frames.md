---
description: Trabajar con fotogramas de vídeo
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Trabajar con fotogramas de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274948"
---
# <a name="working-with-video-frames"></a>Trabajar con fotogramas de vídeo

El vídeo sin comprimir es una secuencia de mapas de bits que se reproducen en una sucesión rápida, normalmente a una velocidad de unos 30 fotogramas por segundo. Dado que la mayoría de los vídeos DirectShow gráfico de filtro en un formato comprimido, la secuencia de vídeo suele pasar a través de un descodificador para la descompresión. Muchos descodificadores emiten datos en formato YUV y dejan la conversión final a RGB para el hardware de vídeo justo antes de la representación. Si un descodificador usa la aceleración de vídeo de DirectX, el hardware de vídeo realiza un trabajo adicional para descodificar la imagen. Por lo tanto, es posible que la descompresión final de los mapas de bits no se realice hasta que los datos lleguen al hardware de vídeo.

Pero para realizar muchos tipos de análisis, procesamiento o edición de vídeo, a menudo es necesario trabajar en mapas de bits sin comprimir en algún tipo de formato RGB o YUV antes de que se representen o escriban en el archivo. Este trabajo se realiza normalmente dentro de un filtro de transformación basado en la clase base [**CTransformFilter,**](ctransformfilter.md) específicamente en el **método Transform.** Este método recibe un puntero a un [**objeto IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) que encapsula los datos de vídeo. El **método IMediaSample::GetPointer** devuelve un puntero al primer byte de los datos sin procesar. En el caso de los fotogramas sin comprimir, estos datos constan de píxeles a los que el filtro puede acceder o modificar directamente. En las secciones siguientes se proporciona información general que le ayudará a trabajar eficazmente con datos DIB de esta manera.

> [!Note]  
> También puede modificar los bits mediante las funciones GDI, GDI+, DirectDraw o Direct3D, pero estas técnicas están fuera del ámbito de este artículo.

 

Esta sección contiene los siguientes temas:

-   [De arriba abajo frente a Bottom-Up DIB](top-down-vs--bottom-up-dibs.md)
-   [Trabajar con RGB de 16 bits](working-with-16-bit-rgb.md)

 

 



