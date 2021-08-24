---
description: Ejemplo de filtro de volcado
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Ejemplo de filtro de volcado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5643f0334071b8c238a70ed31eee87de4e93e3637b5403d886d79f2816e39c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148738"
---
# <a name="dump-filter-sample"></a>Ejemplo de filtro de volcado

## <a name="description"></a>Descripción

El filtro de volcado es un filtro de representador que escribe los ejemplos multimedia que recibe en un archivo de texto.

En este ejemplo se muestra cómo usar la clase de filtro base [**CBaseFilter**](cbasefilter.md) y la clase de pin de entrada [**representada CRenderedInputPin**](crenderedinputpin.md). También se muestra cómo implementar la [**interfaz IFileSinkFilter.**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) El filtro volcado tiene un único pin de entrada, que escribe cada ejemplo que recibe directamente en un archivo.

## <a name="usage"></a>Uso

Este filtro es una herramienta de depuración útil. Por ejemplo, puede comprobar, bit a bit, los resultados de un filtro de transformación. Puede compilar un grafo manualmente mediante GraphEdit y conectar el filtro volcado a la salida de un filtro de transformación o cualquier otro pin de salida. También puede conectar un filtro de tee y colocar el filtro de volcado en una parte del filtro de tee y la salida típica en otra para supervisar los resultados en un escenario en tiempo real.

## <a name="downloading-the-sample"></a>Descargar el ejemplo

Para descargar los ejemplos DirectShow SDK, instale la versión más reciente [de Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Este ejemplo se instala en la siguiente ruta de acceso: *\[ SDK \] Root* Samples Multimedia DirectShow Filters \\ \\ \\ \\ \\ Dump./

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Muestras](directshow-samples.md)
</dt> </dl>

 

 



