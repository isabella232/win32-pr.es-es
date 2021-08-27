---
description: Formatos de tiempo para los comandos seek
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Formatos de tiempo para los comandos seek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e585a7dda12b40e7f501e51aff6ffed50d647066f03804c82e5ffa236f8623a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078725"
---
# <a name="time-formats-for-seek-commands"></a>Formatos de tiempo para los comandos seek

Muchos de los métodos de la **interfaz IMediaSeeking** tienen parámetros que expresan valores de posición, como la posición actual o la posición de detenerse. De forma predeterminada, estos parámetros se expresan en unidades de 100 nanosegundos, también denominado tiempo de referencia. Cualquier filtro que pueda buscar debe admitir la búsqueda por hora de referencia. Algunos filtros también pueden buscar mediante otras unidades de tiempo, como buscar un número de fotograma determinado o buscar un desplazamiento de bytes determinado dentro de una secuencia. Cada una de estas unidades de tiempo se denomina formato de hora y se define mediante un identificador único global (GUID). Para obtener una lista de los formatos de hora definidos por DirectShow, vea GUID [**de formato de hora**](time-format-guids.md). Los terceros también pueden definir GUID para formatos de tiempo personalizados.

Para determinar si los filtros que se encuentran actualmente en el gráfico de filtros admiten un formato de hora determinado, llame al método [**IMediaSeeking::IsFormatSupported.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) El método devuelve S \_ OK si se admite el formato. De lo contrario, devuelve S \_ FALSE o un código de error. Si se admite un formato, puede cambiar a ese formato llamando al método [**IMediaSeeking::SetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) Si el **método SetTimeFormat** se realiza correctamente, los comandos seek posteriores se expresan con el nuevo formato de hora.

En el ejemplo siguiente se comprueba si el gráfico admite la búsqueda por número de fotograma. Si es así, busca enmarcar el número 20:


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



Tenga en cuenta que los formatos de tiempo solo se aplican a los comandos de búsqueda. No afectan a la reproducción del grafo ni a otras acciones.

 

 



