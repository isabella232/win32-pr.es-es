---
description: Hay varios tipos de consultas que se han diseñado para consultar el estado de los recursos.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Consultas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906324"
---
# <a name="queries-direct3d-9"></a>Consultas (Direct3D 9)

Hay varios tipos de consultas que se han diseñado para consultar el estado de los recursos. El estado de un recurso determinado incluye el estado de la unidad de procesamiento de gráficos (GPU), el estado del controlador o el estado en tiempo de ejecución. Para comprender la diferencia entre los distintos tipos de consulta, debe comprender los Estados de la consulta. En el siguiente diagrama de transición de estado se explica cada uno de los Estados de la consulta.

![diagrama que muestra las transiciones entre Estados de consulta](images/queries.png)

En el diagrama se muestran tres Estados, cada uno definido por círculos. Cada una de las líneas sólidas son eventos controlados por la aplicación que causan una transición de estado. La línea discontinua es un evento controlado por recursos que cambia una consulta del estado emitido al estado señalado. Cada uno de estos Estados tiene un propósito diferente:

-   El estado señalado es como un estado de inactividad. El objeto de consulta se ha generado y está esperando a que la aplicación emita la consulta. Una vez que se completa una consulta y se vuelve a pasar al estado señalado, se puede recuperar la respuesta a la consulta.
-   El estado de creación es como un área de ensayo para una consulta. Desde el estado de compilación, se ha emitido una consulta (llamando a [**D3DISSUE \_ Begin**](d3dissue-begin.md)) pero aún no ha pasado al estado emitido. Cuando una aplicación emite un final de consulta (mediante una llamada a [**D3DISSUE \_ End**](d3dissue-end.md)), la consulta pasa al estado emitido.
-   El estado emitido significa que el recurso que se consulta tiene el control de la consulta. Una vez que el recurso finaliza su trabajo, el recurso realiza la transición de la máquina de Estados al estado señalado. Durante el estado emitido, la aplicación debe sondear para detectar la transición al estado señalado. Una vez que se produce la transición al estado señalado, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) devuelve el resultado de la consulta (a través de un argumento) a la aplicación.

En la tabla siguiente se enumeran los tipos de consulta disponibles.



| Tipo de consulta        | Evento Issue                                                                      | Búfer GetData                                                              | Tiempo de ejecución      | Inicio implícito de la consulta                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| BANDWIDTHTIMINGS  | [**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**](d3ddevinfo-d3d9bandwidthtimings.md) | Venta directa/depuración | N/D                                              |
| CACHEUTILIZATION  | [**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9CACHEUTILIZATION**](d3ddevinfo-d3d9cacheutilization.md) | Venta directa/depuración | N/D                                              |
| CESO             | [**Final de D3DISSUE \_**](d3dissue-end.md)                                            | BOOL                                                                        | Venta directa/depuración | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| INTERFACETIMINGS  | [**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9INTERFACETIMINGS**](d3ddevinfo-d3d9interfacetimings.md) | Venta directa/depuración | N/D                                              |
| OCULTO         | [**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | DWORD                                                                       | Venta directa/depuración | N/D                                              |
| PIPELINETIMINGS   | [**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9PIPELINETIMINGS**](d3ddevinfo-d3d9pipelinetimings.md)   | Venta directa/depuración | N/D                                              |
| RESOURCEMANAGER   | [**Final de D3DISSUE \_**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md)           | Solo depuración   | [**Presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| timestamp         | [**Final de D3DISSUE \_**](d3dissue-end.md)                                            | UINT64                                                                      | Venta directa/depuración | N/D                                              |
| TIMESTAMPDISJOINT | [**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | BOOL                                                                        | Venta directa/depuración | N/D                                              |
| TIMESTAMPFREQ     | [**Final de D3DISSUE \_**](d3dissue-end.md)                                            | UINT64                                                                      | Venta directa/depuración | N/D                                              |
| VCACHE            | [**Final de D3DISSUE \_**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ VCACHE**](d3ddevinfo-vcache.md)                             | Venta directa/depuración | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| VERTEXSTATS       | [**Final de D3DISSUE \_**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ D3DVERTEXSTATS**](d3ddevinfo-d3dvertexstats.md)             | Solo depuración   | [**Presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| VERTEXTIMINGS     | [**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9STAGETIMINGS**](d3ddevinfo-d3d9stagetimings.md)         | Venta directa/depuración | N/D                                              |



 

Algunas de las consultas requieren un evento Begin y end, mientras que otras solo requieren un evento End. Las consultas que solo requieren un evento End comienzan cuando se produce otro evento implícito (que aparece en la tabla). Todas las consultas devuelven una respuesta, excepto la consulta de eventos cuya respuesta siempre es **true**. Una aplicación utiliza el estado de la consulta o el código de retorno de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).

## <a name="create-a-query"></a>Crear una consulta

Antes de crear una consulta, puede comprobar si el tiempo de ejecución admite consultas llamando a [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) con un puntero **nulo** como este:


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



Este método devuelve un código de operación correcta si se puede crear una consulta; en caso contrario, devuelve un código de error. Una vez que [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) se ejecute correctamente, puede crear un objeto de consulta similar al siguiente:


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



Si la llamada se realiza correctamente, se crea un objeto de consulta. La consulta está esencialmente inactiva en el estado señalado (con una respuesta no inicializada) en espera de ser emitida. Cuando haya terminado con la consulta, suéltelo como cualquier otra interfaz.

## <a name="issue-a-query"></a>Emisión de una consulta

Una aplicación cambia el estado de una consulta mediante la emisión de una consulta. Este es un ejemplo de la emisión de una consulta:


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



Una consulta en el estado señalado pasará a ser similar a la siguiente cuando se emita:



| Tipo de problema                                | Las transiciones de consulta a. . . |
|-------------------------------------------|--------------------------------|
| [**Inicio de D3DISSUE \_**](d3dissue-begin.md) | Estado de compilación.                |
| [**Final de D3DISSUE \_**](d3dissue-end.md)     | Estado emitido.                  |



 

Una consulta en el estado de creación cambiará de este modo cuando se emita:



| Tipo de problema                                | Las transiciones de consulta a. . .                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [**Inicio de D3DISSUE \_**](d3dissue-begin.md) | (Ninguna transición permanece en el estado de compilación. Reinicia el corchete de consulta). |
| [**Final de D3DISSUE \_**](d3dissue-end.md)     | Estado emitido.                                                             |



 

Una consulta en el estado emitido se realizará una transición similar a la siguiente cuando se emita:



| Tipo de problema                                | Las transiciones de consulta a. . .                    |
|-------------------------------------------|---------------------------------------------------|
| [**Inicio de D3DISSUE \_**](d3dissue-begin.md) | Compilar el estado y reinicia el corchete de consulta.    |
| [**Final de D3DISSUE \_**](d3dissue-end.md)     | Estado emitido después de abandonar la consulta existente. |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a>Comprobar el estado de la consulta y obtener la respuesta a la consulta

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) hace dos cosas:

1.  Devuelve el estado de la consulta en el código de retorno.
2.  Devuelve la respuesta a la consulta en *pdata*.

En cada uno de los tres Estados de la consulta, estos son los códigos de retorno [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) :



| Estado de la consulta | Código de retorno GetData |
|-------------|---------------------|
| Señalado    | S \_ correcto               |
| Compilación    | Código de error          |
| Emitido      | S \_ false            |



 

Por ejemplo, cuando una consulta está en el estado emitido y la respuesta a la consulta no está disponible, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) devuelve S \_ false. Cuando el recurso finaliza su trabajo y la aplicación ha emitido un fin de consulta, el recurso realiza la transición de la consulta al estado señalado. En el estado señalado, **GetData** devuelve S, \_ lo que significa que la respuesta a la consulta también se devuelve en *pdata*. Por ejemplo, esta es la secuencia de eventos para devolver el número de píxeles dibujados en una secuencia de representación:

-   Crear la consulta.
-   Emita un evento Begin.
-   Dibuje algo.
-   Emite un evento de finalización.

A continuación se encuentra la secuencia de código correspondiente:


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



Estas líneas de código hacen varias cosas:

-   Llame a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) para devolver el número de píxeles dibujados.
-   Especifique [**el \_ vaciado de D3DGETDATA**](d3dgetdata-flush.md) para permitir que el recurso pase la consulta al estado señalado.
-   Sondee el recurso de consulta mediante una llamada a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) desde un bucle. Siempre que **GetData** devuelva S \_ , esto significa que el recurso aún no ha devuelto la respuesta.

En esencia, el valor devuelto por [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) indica en qué estado se encuentra la consulta. Los valores posibles son \_ OK, s \_ false y un error. No llame a **GetData** en una consulta que se encuentra en el estado de compilación.

-   S \_ correcto significa que el recurso (GPU o controlador o tiempo de ejecución) ha finalizado. La consulta devuelve el estado señalado. La respuesta (si existe) la devuelve [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).
-   S \_ false significa que el recurso (GPU o controlador o tiempo de ejecución) no puede devolver una respuesta todavía. Esto puede deberse a que la GPU no se ha terminado o no ha detectado aún el trabajo.
-   Un error significa que la consulta ha generado un error del que no se puede recuperar. Este podría ser el caso si se pierde el dispositivo durante una consulta. Una vez que una consulta ha generado un error (distinto de S \_ false), se debe volver a crear la consulta, lo que reiniciará la secuencia de consulta desde el estado señalado.

En lugar de especificar el [**\_ vaciado de D3DGETDATA**](d3dgetdata-flush.md), que proporciona información más actualizada, puede proporcionar cero, que es una comprobación más ligera si la consulta está en el estado emitido. Si se proporciona cero, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) no vaciará el búfer de comandos. Por este motivo, se debe tener cuidado para evitar los bucles infinate (consulte **GetData** para obtener más detalles). Dado que el Runtime pone en cola el trabajo en el búfer de comandos, **D3DGETDATA \_ Flush** es un mecanismo para vaciar el búfer de comandos en el controlador (y, por lo tanto, la GPU; consulte generación de perfiles de llamadas de la [API de Direct3D con precisión (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). Durante el vaciado del búfer de comandos, una consulta puede pasar al estado señalado.

## <a name="example-an-event-query"></a>Ejemplo: una consulta de evento

Una consulta de evento no admite un evento Begin.

-   Crear la consulta.
-   Emite un evento de finalización.
-   Sondear hasta que la GPU esté inactiva.
-   Emite un evento de finalización.


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



Esta es la secuencia de comandos que usa una consulta de eventos para generar perfiles de llamadas de la interfaz de programación de aplicaciones (API) (consulte generación de perfiles de llamadas de la [API de Direct3D (Direct3D 9) con precisión](accurately-profiling-direct3d-api-calls.md). Esta secuencia usa marcadores para ayudar a controlar la cantidad de trabajo en el búfer de comandos.

Tenga en cuenta que las aplicaciones deben prestar especial atención al gran costo asociado con el vaciado del búfer de comandos, ya que esto hace que el sistema operativo cambie al modo kernel, lo que incurre en una penalización de rendimiento considerable. Las aplicaciones también deben tener en cuenta la pérdida de ciclos de CPU al esperar a que se completen las consultas.

Las consultas son una optimización que se va a utilizar durante la representación para aumentar el rendimiento. Por lo tanto, no es beneficioso dedicar tiempo a esperar a que finalice una consulta. Si se emite una consulta y los resultados aún no están listos en el momento en que la aplicación los comprueba, el intento de optimización no se realizó correctamente y la representación debería continuar de la forma habitual.

El ejemplo clásico es durante la selección de la oclusión. En lugar del bucle **While** anterior, una aplicación que usa consultas puede implementar la selección de la oclusión para comprobar si una consulta ha finalizado en el momento en que necesita el resultado. Si la consulta no ha finalizado, continúe (como un escenario en el peor de los casos) como si el objeto que se está probando no es ocluidos (es decir, es visible) y lo representa. El código tendría un aspecto similar al siguiente.


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas avanzados](advanced-topics.md)
</dt> </dl>

 

 
