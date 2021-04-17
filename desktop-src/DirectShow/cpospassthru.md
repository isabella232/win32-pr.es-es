---
description: La clase CPosPassThru controla los comandos de búsqueda para los filtros de transformación, pasándolos al siguiente filtro.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: Clase CPosPassThru (Ctlutil. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670905"
---
# <a name="cpospassthru-class"></a>Clase CPosPassThru

![jerarquía de clase base cpospassthru](images/cutil14.png)

La `CPosPassThru` clase controla los comandos de búsqueda para los filtros de transformación, pasándolos al siguiente filtro.

Cuando una aplicación busca el gráfico de filtro, el administrador de gráficos de filtro proporciona el comando de búsqueda a los filtros de representador. El comando se pasa hacia arriba, a través de la clavija de salida de cada filtro hasta que alcanza un filtro que puede ejecutar el comando (si existe). Para obtener más información, vea [Buscar](seeking.md). La `CPosPassThru` clase pasa todos los comandos de búsqueda al terminal de salida en el filtro de nivel superior, como se muestra en el diagrama siguiente.

![la clase cpospassthru envía comandos de búsqueda ascendentes.](images/cpospassthru.png)

Aunque esta clase se proporciona en la biblioteca de clases base, DirectShow también proporciona la misma clase en Quartz.dll. El uso de la versión de Quartz.dll puede reducir ligeramente el tamaño del código en el filtro, porque la clase se carga en tiempo de ejecución desde el archivo DLL. Para usar esa versión, llame a la función [**CreatePosPassThru**](createpospassthru.md) .

En el método **NonDelegatingQueryInterface** del PIN de salida, delegue en el objeto **CPosPassThru** siempre que la interfaz solicitada sea [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) o [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), como se muestra en el código siguiente:


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



Excepto donde se indique lo contrario, todos los métodos [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) y [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) de esta clase llaman al método correspondiente en el PIN conectado y devuelven el resultado.



| Métodos públicos                                                    | Descripción                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CPosPassThru**](cpospassthru-cpospassthru.md)                 | Método de constructor.                                                                                 |
| [**ForceRefresh**](cpospassthru-forcerefresh.md)                 | Obsoleto.                                                                                           |
| [**GetMediaTime**](cpospassthru-getmediatime.md)                 | Recupera las marcas de tiempo en el ejemplo actual. Virtualiza.                                           |
| Métodos IMediaPosition                                            | Descripción                                                                                         |
| [**obtener \_ duración**](cpospassthru-get-duration.md)                | Recupera la duración de la secuencia.                                                               |
| [**Put \_ CurrentPosition**](cpospassthru-put-currentposition.md)  | Establece la posición actual, en relación con la duración total de la secuencia.                            |
| [**obtener \_ StopTime**](cpospassthru-get-stoptime.md)                | Recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.         |
| [**Put \_ StopTime**](cpospassthru-put-stoptime.md)                | Establece la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.              |
| [**obtener \_ PrerollTime**](cpospassthru-get-prerolltime.md)          | Recupera la cantidad de datos que se pondrán en cola antes de la posición inicial.                         |
| [**Put \_ PrerollTime**](cpospassthru-put-prerolltime.md)          | Establece la cantidad de datos que se pondrán en cola antes de la posición inicial.                              |
| [**obtener \_ velocidad**](cpospassthru-get-rate.md)                        | Recupera la velocidad de reproducción.                                                                        |
| [**\_tasa Put**](cpospassthru-put-rate.md)                        | Establece la velocidad de reproducción.                                                                             |
| [**obtener \_ CurrentPosition**](cpospassthru-get-currentposition.md)  | Recupera la posición actual, en relación con la duración total de la secuencia.                       |
| [**CanSeekForward**](cpospassthru-canseekforward.md)             | Determina si la secuencia se puede buscar hacia atrás.                                               |
| [**CanSeekBackward**](cpospassthru-canseekbackward.md)           | Determina si se puede buscar en el flujo hacia delante.                                                |
| Métodos IMediaSeeking                                             | Descripción                                                                                         |
| [**CheckCapabilities**](cpospassthru-checkcapabilities.md)       | Consulta si un flujo tiene capacidades de búsqueda especificadas.                                        |
| [**ConvertTimeFormat**](cpospassthru-converttimeformat.md)       | Convierte de un formato de hora a otro.                                                           |
| [**GetAvailable**](cpospassthru-getavailable.md)                 | Recupera el intervalo de veces que la búsqueda es eficaz.                                         |
| [**GetCapabilities**](cpospassthru-getcapabilities.md)           | Recupera todas las funciones de búsqueda de la secuencia.                                               |
| [**GetCurrentPosition**](cpospassthru-getcurrentposition.md)     | Recupera la posición actual, en relación con la duración total de la secuencia.                       |
| [**GetDuration**](cpospassthru-getduration.md)                   | Recupera la duración de la secuencia.                                                               |
| [**GetPositions**](cpospassthru-getpositions.md)                 | Recupera la posición actual y la posición de detención, en relación con la duración total de la secuencia. |
| [**GetPreroll**](cpospassthru-getpreroll.md)                     | Recupera la cantidad de datos que se pondrán en cola antes de la posición inicial.                         |
| [**GetRate**](cpospassthru-getrate.md)                           | Recupera la velocidad de reproducción.                                                                        |
| [**GetStopPosition**](cpospassthru-getstopposition.md)           | Recupera la hora a la que se detendrá la reproducción, en relación con la duración de la secuencia.         |
| [**GetTimeFormat**](cpospassthru-gettimeformat.md)               | Recupera el formato de hora actual.                                                                  |
| [**IsFormatSupported**](cpospassthru-isformatsupported.md)       | Determina si se admite un formato de hora especificado.                                            |
| [**IsUsingTimeFormat**](cpospassthru-isusingtimeformat.md)       | Determina si un formato de hora especificado es el formato que se está usando actualmente.                          |
| [**QueryPreferredFormat**](cpospassthru-querypreferredformat.md) | Recupera el formato de hora preferido para la secuencia.                                                 |
| [**SetPositions**](cpospassthru-setpositions.md)                 | Establece la posición actual y la posición de detención.                                                    |
| [**SetRate**](cpospassthru-setrate.md)                           | Establece la velocidad de reproducción.                                                                             |
| [**SetTimeFormat**](cpospassthru-settimeformat.md)               | Establece el formato de hora.                                                                               |
| Funciones del asistente                                                  | Descripción                                                                                         |
| [**CreatePosPassThru**](createpospassthru.md)                    | Crea un `CPosPassThru` objeto o [**CRendererPosPassThru**](crendererpospassthru.md) .            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




