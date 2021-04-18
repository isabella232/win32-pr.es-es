---
description: La clase CSourceSeeking es una clase abstracta para implementar búsquedas en filtros de origen con un PIN de salida.
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: Clase CSourceSeeking (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690511"
---
# <a name="csourceseeking-class"></a>Clase CSourceSeeking

![jerarquía de clases csourceseeking](images/cutil15.png)

La clase **CSourceSeeking** es una clase abstracta para implementar búsquedas en filtros de origen con un PIN de salida.

Esta clase es compatible con la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Proporciona implementaciones predeterminadas para todos los métodos **IMediaSeeking** . Las variables miembro protegidas almacenan la hora de inicio, la hora de detención y la tasa actual. De forma predeterminada, el único formato de hora admitido por la clase es el **formato de hora \_ \_ media \_ Time** (unidades 100-nanosegundos). Vea Comentarios para obtener más información.



| Variables de miembro protegidas                                          | Descripción                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**m \_ rtDuration**](csourceseeking-m-rtduration.md)                | Duración de la secuencia.                                                                     |
| [**m \_ rtStart**](csourceseeking-m-rtstart.md)                      | Hora de inicio.                                                                                 |
| [**m \_ rtStop**](csourceseeking-m-rtstop.md)                        | Hora de detención.                                                                                  |
| [**m \_ dRateSeeking**](csourceseeking-m-drateseeking.md)            | Velocidad de reproducción.                                                                              |
| [**m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md)          | Funciones de búsqueda.                                                                       |
| [**m \_ Plock**](csourceseeking-m-plock.md)                          | Puntero a un objeto de sección crítica para el bloqueo.                                           |
| Métodos protegidos                                                   | Descripción                                                                                 |
| [**CSourceSeeking**](csourceseeking-csourceseeking.md)             | Método de constructor.                                                                         |
| Métodos virtuales puros                                                | Descripción                                                                                 |
| [**ChangeRate**](csourceseeking-changerate.md)                     | Se le llama cuando cambia la velocidad de reproducción.                                                      |
| [**Cambie las**](csourceseeking-changestart.md)                   | Se le llama cuando cambia la posición de inicio.                                                     |
| [**ChangeStop**](csourceseeking-changestop.md)                     | Se le llama cuando cambia la posición de detención.                                                      |
| Métodos IMediaSeeking                                               | Descripción                                                                                 |
| [**IsFormatSupported**](csourceseeking-isformatsupported.md)       | Determina si se admite un formato de hora especificado.                                    |
| [**QueryPreferredFormat**](csourceseeking-querypreferredformat.md) | Recupera el formato de hora preferido del objeto.                                               |
| [**SetTimeFormat**](csourceseeking-settimeformat.md)               | Establece el formato de hora.                                                                       |
| [**IsUsingTimeFormat**](csourceseeking-isusingtimeformat.md)       | Determina si un formato de hora especificado es el formato que se está usando actualmente.                  |
| [**GetTimeFormat**](csourceseeking-gettimeformat.md)               | Recupera el formato de hora actual.                                                          |
| [**GetDuration**](csourceseeking-getduration.md)                   | Recupera la duración de la secuencia.                                                       |
| [**GetStopPosition**](csourceseeking-getstopposition.md)           | Recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia. |
| [**GetCurrentPosition**](csourceseeking-getcurrentposition.md)     | Recupera la posición actual, en relación con la duración total de la secuencia.               |
| [**GetCapabilities**](csourceseeking-getcapabilities.md)           | Recupera todas las funciones de búsqueda de la secuencia.                                       |
| [**CheckCapabilities**](csourceseeking-checkcapabilities.md)       | Consulta si la secuencia tiene capacidades de búsqueda especificadas.                              |
| [**ConvertTimeFormat**](csourceseeking-converttimeformat.md)       | Convierte de un formato de hora a otro.                                                   |
| [**SetPositions**](csourceseeking-setpositions.md)                 | Establece la posición actual y la posición de detención.                                            |
| [**GetPositions**](csourceseeking-getpositions.md)                 | Recupera la posición actual y la posición de detención.                                       |
| [**GetAvailable**](csourceseeking-getavailable.md)                 | Recupera el intervalo de veces que la búsqueda es eficaz.                                 |
| [**SetRate**](csourceseeking-setrate.md)                           | Establece la velocidad de reproducción.                                                                     |
| [**GetRate**](csourceseeking-getrate.md)                           | Recupera la velocidad de reproducción.                                                                |
| [**GetPreroll**](csourceseeking-getpreroll.md)                     | Recupera el tiempo de prelanzamiento.                                                                 |



 

## <a name="remarks"></a>Observaciones

Cuando cambia la posición de inicio, la posición de detención o la velocidad de reproducción, el objeto **CSourceSeeking** llama al método virtual puro correspondiente:

-   Posición inicial: [ **CSourceSeeking:: cambie las**](csourceseeking-changestart.md)
-   Posición de detención: [ **CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md)
-   Velocidad de reproducción: [ **CSourceSeeking:: ChangeRate**](csourceseeking-changerate.md)

La clase derivada debe implementar estos métodos. Después de cualquier operación de búsqueda, un filtro debe hacer lo siguiente:

1.  Llame al método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el PIN de entrada de nivel inferior.
2.  Detenga el subproceso de trabajo que está entregando datos.
3.  Llame al método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en el PIN de entrada.
4.  Reinicie el subproceso de trabajo.
5.  Llame al método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) en el PIN de entrada.
6.  Establezca la propiedad discontinuidad en el primer ejemplo. Llame al método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .

La llamada a [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) libera el subproceso de trabajo, si el subproceso está bloqueado en espera para ofrecer un ejemplo.

En el paso 2, asegúrese de que el subproceso ha dejado de enviar datos. Dependiendo de la implementación, puede que tenga que esperar a que el subproceso se cierre o para que el subproceso señale una respuesta de algún tipo. Si el filtro usa la clase [**CSourceStream**](csourcestream.md) , el método [**CSourceStream:: Stop**](csourcestream-stop.md) se bloquea hasta que el subproceso de trabajo responde.

Idealmente, el nuevo segmento (paso 5) debe entregarse desde el subproceso de trabajo. También lo puede hacer el objeto **CSourceSeeking** , siempre y cuando el filtro lo serialice con los ejemplos.

En el ejemplo siguiente se muestra una posible implementación. Se supone que el PIN de salida del filtro de origen se deriva de **CSourceSeeking** y [**CSourceStream**](csourcestream.md). En este ejemplo se define un método auxiliar, UpdateFromSeek, que realiza los pasos 1 4. El método [**CSourceStream:: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) se invalida para enviar el nuevo segmento y para establecer una marca que indica la discontinuidad. El subproceso de trabajo recoge esta marca y llama al método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) :


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a>Compatibilidad con formatos de hora adicionales

De forma predeterminada, esta clase admite la búsqueda solo en unidades de tiempo de referencia ( \_ tiempo medio de formato de tiempo \_ \_ ). Para admitir formatos de hora adicionales, invalide los métodos de [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) que se ocupan de los formatos de hora:

-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Además, invalide los métodos [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) restantes para realizar las conversiones necesarias entre los formatos de hora. Después de llamar al método [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) , todos los métodos **IMediaSeeking** deben tratar los parámetros de tiempo de entrada y de salida como si estuvieran en el nuevo formato de hora. Por ejemplo, si la variable *m \_ rtDuration* representa la duración en unidades de tiempo de referencia, pero el formato de hora actual es fotogramas, el método [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) debe devolver el valor *m \_ rtDuration* convertido a fotogramas. Por ejemplo:


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



Además, asegúrese de comprobar la \_ marca AM Seek \_ ReturnTime en el método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) . Si este marcador está presente, convierta los valores de posición en tiempos de referencia cuando los devuelva al autor de la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Admitir búsquedas en un filtro de origen](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




