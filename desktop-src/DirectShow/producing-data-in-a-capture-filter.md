---
description: En este tema se describe cómo un filtro de captura DirectShow personalizado debe generar datos de salida.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Generar datos en un filtro de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160127"
---
# <a name="producing-data-in-a-capture-filter"></a>Generar datos en un filtro de captura

En este tema se describe cómo un filtro de captura DirectShow personalizado debe generar datos de salida.

## <a name="filter-state-changes"></a>Filtrar cambios de estado

Un filtro de captura solo debe generar datos cuando el filtro se está ejecutando. No envíe datos desde los pines cuando el filtro esté en pausa. Además, devuelve **VFW \_ S \_ CANT \_ CUE** desde el [**método CBaseFilter::GetState**](cbasefilter-getstate.md) cuando el filtro está en pausa. Este valor devuelto informa al Administrador de Graph que no debe esperar ningún dato del filtro mientras el filtro está en pausa. Para obtener más información, vea [Estados de filtro](filter-states.md).

El código siguiente muestra cómo implementar el [**método IMediaFilter::GetState:**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate)


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



## <a name="controlling-individual-streams"></a>Controlar las Secuencias

Los pines de salida de un filtro de captura deben admitir la interfaz [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) para que una aplicación pueda activar o desactivar cada pin individualmente. Por ejemplo, una aplicación puede obtener una vista previa sin capturar y, a continuación, cambiar al modo de captura sin volver a generar el gráfico de filtros. Puede usar la [**clase CBaseStreamControl**](cbasestreamcontrol.md) para implementar esta interfaz.

## <a name="time-stamps"></a>Marcas de tiempo

Cuando el filtro captura una muestra, marca de tiempo la muestra con el tiempo de secuencia actual. La hora de finalización es la hora de inicio más la duración. Por ejemplo, si el filtro captura diez muestras por segundo y el tiempo de transmisión es de 200 000 000 unidades cuando el filtro captura la muestra, las marcas de tiempo deben ser 200000000 y 201000000. (Hay 10 000 000 unidades por segundo).

Para calcular el tiempo de secuencia, llame al método [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) para obtener la hora de referencia actual y, a continuación, sustrae la hora de inicio original. Como alternativa, llame [**al método CBaseFilter::StreamTime,**](cbasefilter-streamtime.md) que realiza el mismo cálculo. Para establecer la marca de tiempo en un ejemplo, llame al [**método IMediaSample::SetTime.**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime)

Sin embargo, si el filtro tiene un pin de vista previa, los ejemplos del pin de vista previa no deben tener marcas de tiempo. El motivo es que las muestras siempre llegarán al representador ligeramente después del tiempo de captura. Si las muestras tienen una marca de tiempo, el representador las tratará como tardías y puede intentar ponerse al día quitando muestras. (Para obtener más información, [vea DirectShow filtros de captura de vídeo).](directshow-video-capture-filters.md) Tenga en cuenta que [**la interfaz IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) requiere el pin para realizar un seguimiento de los tiempos de ejemplo. Para una marca de vista previa, es posible que tenga que modificar la implementación para que no se base en marcas de tiempo.

Las marcas de tiempo siempre deben aumentar de una muestra a la siguiente. Esto es así incluso cuando se pausa el filtro. Si el filtro se ejecuta, se pausa y, a continuación, se ejecuta de nuevo, el primer ejemplo después de la pausa debe tener una marca de tiempo mayor que la última muestra anterior a la pausa.

En función de los datos que capture, puede ser adecuado establecer el tiempo de los medios en los ejemplos.

Para obtener más información, [vea Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros de captura de vídeo](directshow-video-capture-filters.md)
</dt> <dt>

[Hora y relojes en DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Escribir filtros de captura](writing-capture-filters.md)
</dt> </dl>

 

 



