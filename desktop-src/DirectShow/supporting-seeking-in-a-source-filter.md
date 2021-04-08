---
description: En este tema se describe cómo implementar búsquedas en un filtro de origen de Microsoft DirectShow. Usa el ejemplo de filtro de bola como punto de partida y describe el código adicional necesario para admitir la búsqueda en este filtro.
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: Admitir búsquedas en un filtro de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ac4bbb63410adf9cb4e8d69064679143b84d67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913138"
---
# <a name="supporting-seeking-in-a-source-filter"></a>Admitir búsquedas en un filtro de origen

En este tema se describe cómo implementar búsquedas en un filtro de origen de Microsoft DirectShow. Usa el ejemplo de [filtro de bola](ball-filter-sample.md) como punto de partida y describe el código adicional necesario para admitir la búsqueda en este filtro.

El ejemplo de [filtro de bola](ball-filter-sample.md) es un filtro de origen que crea una bola de rebote animado. En este artículo se describe cómo agregar funcionalidad de búsqueda a este filtro. Una vez que haya agregado esta funcionalidad, puede representar el filtro en GraphEdit y controlar la bola arrastrando el control deslizante de GraphEdit.

Este tema contiene las siguientes secciones:

-   [Información general sobre la búsqueda en DirectShow](#overview-of-seeking-in-directshow)
-   [Información general rápida del filtro de bola](#quick-overview-of-the-ball-filter)
-   [Modificar el filtro de bola para búsquedas](#modifying-the-ball-filter-for-seeking)
-   [Limitaciones de la clase CSourceSeeking](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a>Información general sobre la búsqueda en DirectShow

Una aplicación busca el gráfico de filtro llamando a un método [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) en el administrador de gráficos de filtro. A continuación, el administrador de gráficos de filtro distribuye la llamada a cada representador del gráfico. Cada representador envía la llamada ascendente, a través del PIN de salida del siguiente filtro de nivel superior. La llamada viaja hacia arriba hasta que alcanza un filtro que puede ejecutar el comando Seek, normalmente un filtro de origen o un filtro de analizador. En general, el filtro que origina las marcas de tiempo también controla las operaciones de búsqueda.

Un filtro responde a un comando de búsqueda de la manera siguiente:

1.  El filtro vacía el gráfico. Esto borra los datos obsoletos de Graph, lo que mejora la capacidad de respuesta. De lo contrario, es posible que se entreguen los ejemplos que se almacenaron en búfer antes del comando Seek.
2.  El filtro llama a [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) para informar a los filtros de nivel inferior de la nueva hora de detención, la hora de inicio y la velocidad de reproducción.
3.  Después, el filtro establece la marca de discontinuidad en el primer ejemplo después del comando Seek.

Las marcas de tiempo comienzan desde cero después de cualquier comando de búsqueda (incluidos los cambios de velocidad).

## <a name="quick-overview-of-the-ball-filter"></a>Información general rápida del filtro de bola

El filtro de bola es un origen de inserción, lo que significa que usa un subproceso de trabajo para proporcionar ejemplos de bajada, en lugar de un origen de extracción, que espera pasivamente a que un filtro de nivel inferior solicite ejemplos. El filtro Ball se genera a partir de la clase [**CSource**](csource.md) y su PIN de salida se genera a partir de la clase [**CSourceStream**](csourcestream.md) . La clase **CSourceStream** crea el subproceso de trabajo que controla el flujo de datos. Este subproceso entra en un bucle que obtiene ejemplos del asignador, los rellena con datos y los entrega de nivel inferior.

La mayor parte de la acción en [**CSourceStream**](csourcestream.md) se produce en el método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , que implementa la clase derivada. El argumento de este método es un puntero al ejemplo que se va a entregar. La implementación del filtro de bola de **FillBuffer** recupera la dirección del búfer de ejemplo y dibuja directamente en el búfer estableciendo valores de píxel individuales. (El dibujo lo realiza una clase auxiliar, CBall, por lo que puede omitir los detalles relacionados con la profundidad de bits, las paletas, etc.).

## <a name="modifying-the-ball-filter-for-seeking"></a>Modificar el filtro de bola para búsquedas

Para que el filtro de bola sea buscable, use la clase [**CSourceSeeking**](csourceseeking.md) , que está diseñada para implementar búsquedas en filtros con un PIN de salida. Agregue la clase **CSourceSeeking** a la lista de herencia de la clase CBallStream:


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



Además, tendrá que agregar un inicializador para [**CSourceSeeking**](csourceseeking.md) al constructor CBallStream:


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



Esta instrucción llama al constructor base de [**CSourceSeeking**](csourceseeking.md). Los parámetros son un nombre, un puntero al pin propietario, un valor **HRESULT** y la dirección de un objeto de sección crítica. El nombre solo se usa para la depuración y la macro [**Name**](name.md) se compila en una cadena vacía en las compilaciones comerciales. El PIN hereda directamente **CSourceSeeking**, por lo que el segundo parámetro es un puntero a sí mismo, convertido a un puntero [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) . El valor **HRESULT** se omite en la versión actual de las clases base; sigue siendo compatible con las versiones anteriores. La sección crítica protege los datos compartidos, como la hora de inicio actual, la hora de finalización y la velocidad de reproducción.

Agregue la siguiente instrucción en el constructor [**CSourceSeeking**](csourceseeking.md) :


```C++
m_rtStop = 60 * UNITS;
```



La variable *m \_ rtStop* especifica la hora de detención. De forma predeterminada, el valor es \_ I64 \_ Max/2, que es aproximadamente 14.600 años. La instrucción anterior lo establece en un 60 segundos más conservador.

Se deben agregar dos variables de miembro adicionales a CBallStream:


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



Después de cada comando de búsqueda, el filtro debe establecer la marca de discontinuidad en el ejemplo siguiente mediante una llamada a [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity). La variable *m \_ bDiscontinuity* realizará un seguimiento de este. La variable *m \_ rtBallPosition* especificará la posición de la bola dentro del fotograma de vídeo. El filtro de bola original calcula la posición de la secuencia, pero el tiempo de la secuencia se restablece en cero después de cada comando de búsqueda. En un flujo de búsqueda, la posición absoluta es independiente del tiempo de flujo.

### <a name="queryinterface"></a>QueryInterface

La clase [**CSourceSeeking**](csourceseeking.md) implementa la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Para exponer esta interfaz a los clientes, invalide el método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) :


```C++
STDMETHODIMP CBallStream::NonDelegatingQueryInterface
    (REFIID riid, void **ppv)
{
    if( riid == IID_IMediaSeeking ) 
    {
        return CSourceSeeking::NonDelegatingQueryInterface( riid, ppv );
    }
    return CSourceStream::NonDelegatingQueryInterface(riid, ppv);
}
```



El método se denomina "sin delegación" debido a la manera en que las clases base de DirectShow admiten la agregación del modelo de objetos componentes (COM). Para obtener más información, vea el tema acerca de cómo implementar IUnknown en el SDK de DirectShow.

### <a name="seeking-methods"></a>Métodos de búsqueda

La clase [**CSourceSeeking**](csourceseeking.md) mantiene varias variables de miembro relacionadas con la búsqueda.



| Variable          | Descripción   | Valor predeterminado  |
|-------------------|---------------|----------------|
| *m \_ rtStart*      | Hora de inicio    | Cero           |
| *m \_ rtStop*       | Hora de detención     | \_I64 \_ Max/2 |
| *m \_ dRateSeeking* | Velocidad de reproducción | 1,0            |



 

La implementación de [**CSourceSeeking**](csourceseeking.md) de [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) actualiza las horas de inicio y de finalización y, a continuación, llama a dos métodos virtuales puros en la clase derivada, [**CSourceSeeking:: cambie las**](csourceseeking-changestart.md) y [**CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md). La implementación de [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) es similar: actualiza la velocidad de reproducción y, a continuación, llama al método virtual puro [**CSourceSeeking:: ChangeRate**](csourceseeking-changerate.md). En cada uno de estos métodos virtuales, el PIN debe hacer lo siguiente:

1.  Llame a [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) para iniciar el vaciado de datos.
2.  Detenga el subproceso de streaming.
3.  Llame a [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
4.  Reinicie el subproceso de streaming.
5.  Llame a [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).
6.  Establezca la marca de discontinuidad en el ejemplo siguiente.

El orden de estos pasos es fundamental, ya que el subproceso de streaming puede bloquearse mientras espera para ofrecer un ejemplo u obtener un nuevo ejemplo. El método [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) garantiza que el subproceso de streaming no está bloqueado y, por lo tanto, no interbloqueará en el paso 2. La llamada a [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) informa a los filtros de nivel inferior para que esperen nuevos ejemplos, por lo que no los rechazan cuando el subproceso vuelve a iniciarse en el paso 4.

El siguiente método privado realiza los pasos 1 a 4:


```C++
void CBallStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        // Shut down the thread and stop pushing data.
        Stop();
        DeliverEndFlush();
        // Restart the thread and start pushing data again.
        Pause();
    }
}
```



Cuando el subproceso de streaming se vuelve a iniciar, llama al método [**CSourceStream:: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) . Invalide este método para realizar los pasos 5 y 6:


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



En el método [**cambie las**](csourceseeking-changestart.md) , establezca la hora de la secuencia en cero y la posición de la bola en la nueva hora de inicio. Después, llame a CBallStream:: UpdateFromSeek:


```C++
HRESULT CBallStream::ChangeStart( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_rtSampleTime = 0;
        m_rtBallPosition = m_rtStart;
    }
    UpdateFromSeek();
    return S_OK;
}
```



En el método [**ChangeStop**](csourceseeking-changestop.md) , llame a CBallStream:: UpdateFromSeek si la nueva hora de detención es menor que la posición actual. De lo contrario, la hora de detención todavía está en el futuro, por lo que no es necesario vaciar el gráfico.


```C++
HRESULT CBallStream::ChangeStop( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        if (m_rtBallPosition < m_rtStop)
        {
            return S_OK;
        }
    }

    // We're already past the new stop time. Flush the graph.
    UpdateFromSeek();
    return S_OK;
}
```



En el caso de los cambios de velocidad, el método [**CSourceSeeking:: SetRate**](csourceseeking-setrate.md) establece *m \_ dRateSeeking* en la nueva velocidad (descartando el valor anterior) antes de llamar a [**ChangeRate**](csourceseeking-changerate.md). Desafortunadamente, si el autor de la llamada dio una tasa no válida (por ejemplo, menor que cero), es demasiado tarde en el momento en que se llama a **ChangeRate** . Una solución consiste en invalidar **SetRate** y comprobar las tarifas válidas:


```C++
HRESULT CBallStream::SetRate(double dRate)
{
    if (dRate <= 1.0)
    {
        return E_INVALIDARG;
    }
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_dRateSeeking = dRate;
    }
    UpdateFromSeek();
    return S_OK;
}
// Now ChangeRate won't ever be called, but it's pure virtual, so it needs
// a dummy implementation.
HRESULT CBallStream::ChangeRate() { return S_OK; }
```



### <a name="drawing-in-the-buffer"></a>Dibujar en el búfer

Esta es la versión modificada de [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md), la rutina que dibuja la bola en cada fotograma:


```C++
HRESULT CBallStream::FillBuffer(IMediaSample *pMediaSample)
{
    BYTE *pData;
    long lDataLen;
    pMediaSample->GetPointer(&pData);
    lDataLen = pMediaSample->GetSize();
    {
        CAutoLock cAutoLockShared(&m_cSharedState);
        if (m_rtBallPosition >= m_rtStop) 
        {
            // End of the stream.
            return S_FALSE;
        }
        // Draw the ball in its current position.
        ZeroMemory( pData, lDataLen );
        m_Ball->MoveBall(m_rtBallPosition);
        m_Ball->PlotBall(pData, m_BallPixel, m_iPixelSize);
        
        // The sample times are modified by the current rate.
        REFERENCE_TIME rtStart, rtStop;
        rtStart = static_cast<REFERENCE_TIME>(
                      m_rtSampleTime / m_dRateSeeking);
        rtStop  = rtStart + static_cast<int>(
                      m_iRepeatTime / m_dRateSeeking);
        pMediaSample->SetTime(&rtStart, &rtStop);

        // Increment for the next loop.
        m_rtSampleTime += m_iRepeatTime;
        m_rtBallPosition += m_iRepeatTime;
    }
    pMediaSample->SetSyncPoint(TRUE);
    if (m_bDiscontinuity) 
    {
        pMediaSample->SetDiscontinuity(TRUE);
        m_bDiscontinuity = FALSE;
    }
    return NOERROR;
}
```



Las principales diferencias entre esta versión y la original son las siguientes:

-   Como se mencionó anteriormente, la variable *m \_ rtBallPosition* se usa para establecer la posición de la bola, en lugar de la hora de la secuencia.
-   Después de mantener la sección crítica, el método comprueba si la posición actual supera la hora de detención. Si es así, devuelve **S \_ false**, que indica a la clase base que detenga el envío de datos y entregue una notificación de final de secuencia.
-   Las marcas de tiempo se dividen por la velocidad actual.
-   Si *m \_ BDiscontinuity* es **true**, el método establece la marca de discontinuidad en el ejemplo.

Hay otra diferencia secundaria. Dado que la versión original se basa en tener exactamente un búfer, rellena todo el búfer con ceros una vez, cuando comienza el streaming. Después, simplemente borra la bola de su posición anterior. Sin embargo, esta optimización revela un ligero error en el filtro de bola. Cuando el método [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) llama a [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), establece la marca de solo lectura en **false**. Como resultado, el filtro de nivel inferior es libre de escribir en el búfer. Una solución consiste en invalidar **DecideAllocator** para que establezca la marca de solo lectura en **true**. Para simplificar, sin embargo, la nueva versión simplemente quita la optimización por completo. En su lugar, esta versión rellena el búfer con ceros cada vez.

### <a name="miscellaneous-changes"></a>Cambios varios

En la nueva versión, estas dos líneas se quitan del constructor CBall:


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



El filtro de bola original utiliza estos valores para agregar cierta aleatoriedad a la posición inicial de la bola. Para nuestros propósitos, queremos que la bola sea determinista. Además, se han cambiado algunas variables de los objetos [**CRefTime**](creftime.md) a variables de [**\_ tiempo de referencia**](reference-time.md) . (La clase **CRefTime** es un contenedor fino para un valor de **\_ hora de referencia** ). Por último, la implementación de [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) se ha modificado ligeramente; puede hacer referencia al código fuente para obtener más información.

## <a name="limitations-of-the-csourceseeking-class"></a>Limitaciones de la clase CSourceSeeking

La clase [**CSourceSeeking**](csourceseeking.md) no está diseñada para los filtros con varios PIN de salida, debido a problemas con la comunicación entre PIN. Por ejemplo, Imagine un filtro de analizador que reciba una secuencia de audio y vídeo intercalada, divida el flujo en sus componentes de audio y vídeo, y entregue el vídeo de un PIN de salida y el audio de otro. Ambos pines de salida recibirán todos los comandos de búsqueda, pero el filtro solo debe buscar una vez por cada comando de búsqueda. La solución consiste en designar uno de los pin para controlar la búsqueda y omitir los comandos de búsqueda recibidos por el otro PIN.

Sin embargo, después del comando Seek, ambos PIN deben vaciar los datos. Para complicar aún más los aspectos, el comando Seek se produce en el subproceso de la aplicación, no en el subproceso de streaming. Por lo tanto, debe asegurarse de que ninguno de los pin esté bloqueado y en espera de que se devuelva una llamada [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) , o podría producirse un interbloqueo. Para obtener más información sobre el vaciado seguro para subprocesos en PIN, vea [subprocesos y secciones críticas](threads-and-critical-sections.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de origen](writing-source-filters.md)
</dt> </dl>

 

 



