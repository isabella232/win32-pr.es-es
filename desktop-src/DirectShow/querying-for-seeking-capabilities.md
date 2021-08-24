---
description: Consulta de funcionalidades de búsqueda
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Consulta de funcionalidades de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1d4389d9e5fcf1466a039ae48bbffb2c26a41c29281101984f6a7a291789f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747455"
---
# <a name="querying-for-seeking-capabilities"></a>Consulta de funcionalidades de búsqueda

Microsoft® DirectShow® admite la búsqueda a través de la [**interfaz IMediaSeeking.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) El Administrador Graph filtros expone esta interfaz, pero la funcionalidad de búsqueda siempre se implementa mediante filtros en el gráfico.

No se pueden buscar algunos datos. Por ejemplo, no puede buscar una secuencia de vídeo en directo desde una cámara. Sin embargo, si se puede buscar una secuencia, hay varios tipos de búsqueda que podría admitir. Estos incluyen las siguientes:

-   Buscar una posición arbitraria en la secuencia.
-   Recuperación de la duración de la secuencia.
-   Recuperación de la posición actual dentro de la secuencia.
-   Reproducir en orden inverso.

La **interfaz IMediaSeeking** define un conjunto de marcas, [**AM SEEKING SEEKING \_ \_ \_ CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), que describen las posibles funcionalidades de búsqueda. Para recuperar las funcionalidades de la secuencia, llame al [**método IMediaSeeking::GetCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) El método devuelve una combinación bit a bit de marcas. La aplicación puede probarlas mediante el & **(AND** bit a bit). Por ejemplo, el código siguiente comprueba si el gráfico puede buscar una posición arbitraria:


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



