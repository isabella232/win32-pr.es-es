---
description: La clase CPosPassThru controla los comandos de búsqueda para los filtros de transformación, pasandolos de nivel superior al filtro siguiente.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: CPosPassThru (clase, Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261407"
---
# <a name="cpospassthru-class"></a>CPosPassThru (clase)

![Jerarquía de clases base cpospassthru](images/cutil14.png)

Los `CPosPassThru` identificadores de clase buscan comandos para los filtros de transformación, pasandolos de nivel superior al filtro siguiente.

Cuando una aplicación busca el gráfico de filtros, el Administrador de filtros Graph proporciona el comando seek a los filtros del representador. El comando se pasa ascendentemente, a través del pin de salida de cada filtro, hasta que llega a un filtro que puede ejecutar el comando (si existe). Para obtener más información, vea [Buscar](seeking.md). La clase pasa todos los comandos seek al pin de salida en el filtro `CPosPassThru` ascendente, como se muestra en el diagrama siguiente.

![La clase cpospassthru envía comandos seek ascendentes.](images/cpospassthru.png)

Aunque esta clase se proporciona en la biblioteca de clases base, DirectShow también proporciona la misma clase en Quartz.dll. El uso Quartz.dll versión puede reducir ligeramente el tamaño del código en el filtro, ya que la clase se carga en tiempo de ejecución desde el archivo DLL. Para usar esa versión, llame a [**la función CreatePosPassThru.**](createpospassthru.md)

En el método **NonDelegatingQueryInterface** del pin de salida, delegue al objeto **CPosPassThru** siempre que la interfaz solicitada [**sea IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) o [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), como se muestra en el código siguiente:


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



Excepto donde se indica, todos los métodos [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) de esta clase llaman al método correspondiente en el pin conectado y devuelven el resultado.



| Métodos públicos                                                    | Descripción                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CPosPassThru**](cpospassthru-cpospassthru.md)                 | Método constructor.                                                                                 |
| [**ForceRefresh**](cpospassthru-forcerefresh.md)                 | Obsoleto.                                                                                           |
| [**GetMediaTime**](cpospassthru-getmediatime.md)                 | Recupera las marcas de tiempo del ejemplo actual. Virtual.                                           |
| Métodos IMediaPosition                                            | Descripción                                                                                         |
| [**get \_ Duration**](cpospassthru-get-duration.md)                | Recupera la duración de la secuencia.                                                               |
| [**put \_ CurrentPosition**](cpospassthru-put-currentposition.md)  | Establece la posición actual, en relación con la duración total de la secuencia.                            |
| [**get \_ StopTime**](cpospassthru-get-stoptime.md)                | Recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.         |
| [**put \_ StopTime**](cpospassthru-put-stoptime.md)                | Establece la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.              |
| [**get \_ PrerollTime**](cpospassthru-get-prerolltime.md)          | Recupera la cantidad de datos que se pondrán en cola antes de la posición inicial.                         |
| [**put \_ PrerollTime**](cpospassthru-put-prerolltime.md)          | Establece la cantidad de datos que se pondrán en cola antes de la posición inicial.                              |
| [**get \_ Rate**](cpospassthru-get-rate.md)                        | Recupera la velocidad de reproducción.                                                                        |
| [**put \_ Rate**](cpospassthru-put-rate.md)                        | Establece la velocidad de reproducción.                                                                             |
| [**get \_ CurrentPosition**](cpospassthru-get-currentposition.md)  | Recupera la posición actual, en relación con la duración total de la secuencia.                       |
| [**CanSeekForward**](cpospassthru-canseekforward.md)             | Determina si la secuencia se puede buscar hacia atrás.                                               |
| [**CanSeekBackward**](cpospassthru-canseekbackward.md)           | Determina si la secuencia se puede buscar hacia delante.                                                |
| Métodos IMediaSeeking                                             | Descripción                                                                                         |
| [**CheckCapabilities**](cpospassthru-checkcapabilities.md)       | Consulta si una secuencia ha especificado funcionalidades de búsqueda.                                        |
| [**ConvertTimeFormat**](cpospassthru-converttimeformat.md)       | Convierte de un formato de hora a otro.                                                           |
| [**GetAvailable**](cpospassthru-getavailable.md)                 | Recupera el intervalo de veces en que la búsqueda es eficaz.                                         |
| [**GetCapabilities**](cpospassthru-getcapabilities.md)           | Recupera todas las funcionalidades de búsqueda de la secuencia.                                               |
| [**GetCurrentPosition**](cpospassthru-getcurrentposition.md)     | Recupera la posición actual, en relación con la duración total de la secuencia.                       |
| [**GetDuration**](cpospassthru-getduration.md)                   | Recupera la duración de la secuencia.                                                               |
| [**GetPositions**](cpospassthru-getpositions.md)                 | Recupera la posición actual y la posición de detenerse, en relación con la duración total de la secuencia. |
| [**GetPreroll**](cpospassthru-getpreroll.md)                     | Recupera la cantidad de datos que se pondrán en cola antes de la posición inicial.                         |
| [**GetRate**](cpospassthru-getrate.md)                           | Recupera la velocidad de reproducción.                                                                        |
| [**GetStopPosition**](cpospassthru-getstopposition.md)           | Recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.         |
| [**GetTimeFormat**](cpospassthru-gettimeformat.md)               | Recupera el formato de hora actual.                                                                  |
| [**IsFormatSupported**](cpospassthru-isformatsupported.md)       | Determina si se admite un formato de hora especificado.                                            |
| [**IsUsingTimeFormat**](cpospassthru-isusingtimeformat.md)       | Determina si un formato de hora especificado es el formato actualmente en uso.                          |
| [**QueryPreferredFormat**](cpospassthru-querypreferredformat.md) | Recupera el formato de hora preferido para la secuencia.                                                 |
| [**SetPositions**](cpospassthru-setpositions.md)                 | Establece la posición actual y la posición de detenerse.                                                    |
| [**SetRate**](cpospassthru-setrate.md)                           | Establece la velocidad de reproducción.                                                                             |
| [**SetTimeFormat**](cpospassthru-settimeformat.md)               | Establece el formato de hora.                                                                               |
| Funciones del asistente                                                  | Descripción                                                                                         |
| [**CreatePosPassThru**](createpospassthru.md)                    | Crea un `CPosPassThru` objeto [**o CRendererPosPassThru.**](crendererpospassthru.md)            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




