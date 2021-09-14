---
description: Ejemplo de filtro de volcado
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Ejemplo de filtro de volcado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375218"
---
# <a name="dump-filter-sample"></a>Ejemplo de filtro de volcado

## <a name="description"></a>Descripción

El filtro de volcado es un filtro de representador que escribe los ejemplos multimedia que recibe en un archivo de texto.

En este ejemplo se muestra cómo usar la clase de filtro base [**CBaseFilter**](cbasefilter.md) y la clase de pin de entrada [**representada CRenderedInputPin**](crenderedinputpin.md). También muestra cómo implementar la interfaz [**IFileSinkFilter.**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) El filtro Volcado tiene un único pin de entrada, que escribe cada ejemplo que recibe directamente en un archivo.

## <a name="usage"></a>Uso

Este filtro es una herramienta de depuración útil. Por ejemplo, puede comprobar, bit a bit, los resultados de un filtro de transformación. Puede compilar un gráfico manualmente mediante GraphEdit y conectar el filtro Volcado a la salida de un filtro de transformación o cualquier otro pin de salida. También puede conectar un filtro de tee y colocar el filtro volcado en una parte del filtro de tee y la salida típica en otro para supervisar los resultados en un escenario en tiempo real.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente del [SDK de Windows.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Este ejemplo se instala en la siguiente ruta de acceso: *\[ Sdk Root \]* Samples Multimedia DirectShow Filters \\ \\ \\ \\ \\ Dump.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Muestras](directshow-samples.md)
</dt> </dl>

 

 



