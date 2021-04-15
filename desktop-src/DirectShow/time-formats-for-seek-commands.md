---
description: Formatos de hora para comandos de búsqueda
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Formatos de hora para comandos de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547126"
---
# <a name="time-formats-for-seek-commands"></a>Formatos de hora para comandos de búsqueda

Muchos de los métodos de la interfaz **IMediaSeeking** tienen parámetros que expresan valores de posición, como la posición actual o la posición de detención. De forma predeterminada, estos parámetros se expresan en unidades de 100 nanosegundos, también denominadas hora de referencia. Cualquier filtro que pueda buscar debe admitir búsquedas por tiempo de referencia. Algunos filtros pueden buscar también en otras unidades de tiempo, como buscar un número de marco determinado o buscar un desplazamiento de byte determinado dentro de una secuencia. Cada una de estas unidades de tiempo se denomina formato de hora y se define mediante un identificador único global (GUID). Para obtener una lista de los formatos de hora definidos por DirectShow, consulte [**GUID de formato de hora**](time-format-guids.md). Los terceros también pueden definir GUID para los formatos de hora personalizados.

Para determinar si los filtros que se encuentran actualmente en el gráfico de filtros admiten un formato de hora determinado, llame al método [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) . El método devuelve S \_ OK si se admite el formato. De lo contrario, devuelve S \_ false o un código de error. Si se admite un formato, puede cambiar a ese formato llamando al método [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) . Si el método **SetTimeFormat** se ejecuta correctamente, los comandos de búsqueda subsiguientes se expresan con el nuevo formato de hora.

En el ejemplo siguiente se comprueba si el grafo admite búsquedas por número de marco. Si es así, busca el número de marco 20:


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



Tenga en cuenta que los formatos de hora solo se aplican a los comandos de búsqueda. No afectan a la reproducción de gráficos ni a otras acciones.

 

 



