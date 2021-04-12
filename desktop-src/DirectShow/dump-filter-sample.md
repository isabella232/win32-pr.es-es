---
description: Ejemplo de filtro de volcado de memoria
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Ejemplo de filtro de volcado de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537965"
---
# <a name="dump-filter-sample"></a>Ejemplo de filtro de volcado de memoria

## <a name="description"></a>Descripción

El filtro de volcado es un filtro de representador que escribe los ejemplos de medios que recibe en un archivo de texto.

En este ejemplo se muestra cómo usar la clase de filtro base [**CBaseFilter**](cbasefilter.md) y la clase de PIN de entrada representada [**CRenderedInputPin**](crenderedinputpin.md). También se muestra cómo implementar la interfaz [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) . El filtro de volcado tiene un solo PIN de entrada, que escribe cada ejemplo que recibe directamente en un archivo.

## <a name="usage"></a>Uso

Este filtro es una herramienta de depuración útil. Por ejemplo, puede comprobar, bit a bit, los resultados de un filtro de transformación. Puede compilar un gráfico manualmente mediante GraphEdit y conectar el filtro de volcado a la salida de un filtro de transformación o cualquier otro PIN de salida. También puede conectar un filtro tee y colocar el filtro de volcado en un segmento del filtro tee y el resultado típico en otro segmento para supervisar los resultados en un escenario en tiempo real.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ \] raíz del SDK* de filtros de DirectShow de \\ \\ multimedia \\ \\ \\ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de DirectShow](directshow-samples.md)
</dt> </dl>

 

 



