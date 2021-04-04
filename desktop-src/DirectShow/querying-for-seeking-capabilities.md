---
description: Consulta de funcionalidades de búsqueda
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Consulta de funcionalidades de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906743"
---
# <a name="querying-for-seeking-capabilities"></a>Consulta de funcionalidades de búsqueda

Microsoft® DirectShow® admite la búsqueda a través de la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . El administrador de gráficos de filtro expone esta interfaz, pero la funcionalidad de búsqueda siempre se implementa mediante filtros del gráfico.

No se puede buscar en algunos datos. Por ejemplo, no puede buscar una secuencia de vídeo en directo desde una cámara. Sin embargo, si se puede buscar en una secuencia, es posible que se admitan varios tipos de búsquedas. Entre ellas se incluyen las siguientes:

-   Buscar una posición arbitraria en la secuencia.
-   Recuperar la duración de la secuencia.
-   Recuperar la posición actual dentro de la secuencia.
-   Reproducir en orden inverso.

La interfaz **IMediaSeeking** define un conjunto de marcas, [**que \_ buscan \_ \_ funciones de búsqueda**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), que describen las posibles capacidades de búsqueda. Para recuperar las capacidades de la secuencia, llame al método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) . El método devuelve una combinación bit a bit de marcas. La aplicación puede probarla mediante el operador & (and bit **a** bit). Por ejemplo, el código siguiente comprueba si el gráfico puede buscar una posición arbitraria:


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



