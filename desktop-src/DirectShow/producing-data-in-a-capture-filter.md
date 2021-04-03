---
description: En este tema se describe cómo un filtro de captura de DirectShow personalizado debe generar datos de salida.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Generar datos en un filtro de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997893"
---
# <a name="producing-data-in-a-capture-filter"></a>Generar datos en un filtro de captura

En este tema se describe cómo un filtro de captura de DirectShow personalizado debe generar datos de salida.

## <a name="filter-state-changes"></a>Cambiar el estado de los cambios

Un filtro de captura debe generar datos solo cuando se está ejecutando el filtro. No envíe datos desde los pin cuando el filtro esté en pausa. Además, devuelva la **\_ indicación VFW S \_ peralte \_** desde el método [**CBaseFilter:: GetState**](cbasefilter-getstate.md) cuando el filtro esté en pausa. Este valor devuelto informa al administrador de gráficos de filtro que no debe esperar ningún dato del filtro mientras el filtro está en pausa. Para obtener más información, vea [filtrar Estados](filter-states.md).

En el código siguiente se muestra cómo implementar el método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) :


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a>Controlar flujos individuales

Los pin de salida de un filtro de captura deben admitir la interfaz [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , de modo que una aplicación pueda activar o desactivar cada pin individualmente. Por ejemplo, una aplicación puede obtener una vista previa sin captura y, a continuación, cambiar al modo de captura sin volver a generar el gráfico de filtro. Puede usar la clase [**CBaseStreamControl**](cbasestreamcontrol.md) para implementar esta interfaz.

## <a name="time-stamps"></a>Marcas de tiempo

Cuando el filtro captura un ejemplo, marca de tiempo el ejemplo con la hora de la secuencia actual. La hora de finalización es la hora de inicio más la duración. Por ejemplo, si el filtro captura a diez muestras por segundo y el tiempo de secuencia es de 200 millones unidades cuando el filtro captura el ejemplo, las marcas de tiempo deben ser 200 millones y 201 millones. (Hay 10 millones unidades por segundo).

Para calcular el tiempo de transmisión, llame al método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) para obtener la hora de referencia actual y, a continuación, sustrato a la hora de inicio original. También puede llamar al método [**CBaseFilter:: StreamTime**](cbasefilter-streamtime.md) , que realiza el mismo cálculo. Para establecer la marca de tiempo en un ejemplo, llame al método [**IMediaSample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

Sin embargo, si el filtro tiene un PIN de vista previa, los ejemplos del PIN de vista previa no deben tener marcas de tiempo. La razón es que los ejemplos siempre llegarán al representador ligeramente después del tiempo de captura. Si los ejemplos tienen marca de tiempo, el representador los tratará como tardíos y puede intentar ponerse al día mediante la eliminación de ejemplos. (Para obtener más información, consulte [filtros de captura de vídeo de DirectShow](directshow-video-capture-filters.md)). Tenga en cuenta que la interfaz [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) requiere que el PIN realice un seguimiento de las horas de ejemplo. En el caso de un PIN de vista previa, puede que tenga que modificar la implementación para que no se base en las marcas de tiempo.

Las marcas de tiempo siempre deben aumentar de una muestra a la siguiente. Esto es así incluso cuando el filtro se pausa. Si el filtro se ejecuta, se detiene y, a continuación, se ejecuta de nuevo, el primer ejemplo después de la pausa debe tener una marca de tiempo mayor que la última muestra antes de la pausa.

En función de los datos que se van a capturar, puede ser conveniente establecer la hora del medio en los ejemplos.

Para obtener más información, consulte [hora y relojes en DirectShow](time-and-clocks-in-directshow.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de captura de vídeo de DirectShow](directshow-video-capture-filters.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Escribir filtros de captura](writing-capture-filters.md)
</dt> </dl>

 

 



