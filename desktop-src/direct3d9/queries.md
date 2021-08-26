---
description: Hay varios tipos de consultas diseñadas para consultar el estado de los recursos.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Consultas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2113500673def3e2cca5816e534b567a29fc322fb51f853db98eada20ba62674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069004"
---
# <a name="queries-direct3d-9"></a>Consultas (Direct3D 9)

Hay varios tipos de consultas diseñadas para consultar el estado de los recursos. El estado de un recurso determinado incluye el estado de la unidad de procesamiento gráfico (GPU), el estado del controlador o el estado de tiempo de ejecución. Para comprender la diferencia entre los distintos tipos de consulta, debe comprender los estados de consulta. En el siguiente diagrama de transición de estado se explica cada uno de los estados de consulta.

![diagrama que muestra las transiciones entre estados de consulta](images/queries.png)

El diagrama muestra tres estados, cada uno definido por círculos. Cada una de las líneas sólidas son eventos controlados por la aplicación que provocan una transición de estado. La línea discontinua es un evento controlado por recursos que cambia una consulta del estado emitido al estado señalado. Cada uno de estos estados tiene un propósito diferente:

-   El estado señalado es como un estado inactivo. El objeto de consulta se ha generado y está esperando a que la aplicación emita la consulta. Una vez que se ha completado una consulta y ha pasado de nuevo al estado señalado, se puede recuperar la respuesta a la consulta.
-   El estado de creación es como un área de ensayo para una consulta. Desde el estado de creación, se ha emitido una consulta (mediante una llamada a [**D3DISSUE \_ BEGIN**](d3dissue-begin.md)), pero aún no ha pasado al estado emitido. Cuando una aplicación emite un final de consulta (llamando a [**D3DISSUE \_ END),**](d3dissue-end.md)la consulta realiza la transición al estado emitido.
-   El estado emitido significa que el recurso que se consulta tiene el control de la consulta. Una vez que el recurso finaliza su trabajo, el recurso pasa la máquina de estado al estado señalado. Durante el estado emitido, la aplicación debe sondear para detectar la transición al estado señalado. Una vez que se produce la transición al estado señalado, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) devuelve el resultado de la consulta (a través de un argumento) a la aplicación.

En la tabla siguiente se enumeran los tipos de consulta disponibles.



| Tipo de consulta        | Evento de problema                                                                      | Búfer GetData                                                              | Tiempo de ejecución      | Inicio implícito de la consulta                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| BANDWIDTHTIMINGS  | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**](d3ddevinfo-d3d9bandwidthtimings.md) | Retail/Debug | No procede                                              |
| CACHEUTILIZATION  | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9CACHEUTILIZATION**](d3ddevinfo-d3d9cacheutilization.md) | Retail/Debug | No procede                                              |
| Evento             | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | BOOL                                                                        | Retail/Debug | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| INTERFACETIMINGS  | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9INTERFACETIMINGS**](d3ddevinfo-d3d9interfacetimings.md) | Retail/Debug | No procede                                              |
| Oclusión         | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ END**](d3dissue-end.md) | DWORD                                                                       | Retail/Debug | No procede                                              |
| PIPELINETIMINGS   | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9PIPELINETIMINGS**](d3ddevinfo-d3d9pipelinetimings.md)   | Retail/Debug | No procede                                              |
| Resourcemanager   | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md)           | Solo depuración   | [**Presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| timestamp         | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | UINT64                                                                      | Retail/Debug | No procede                                              |
| TIMESTAMPDISJOINT | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ END**](d3dissue-end.md) | BOOL                                                                        | Retail/Debug | No procede                                              |
| TIMESTAMPFREQ     | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | UINT64                                                                      | Retail/Debug | No procede                                              |
| VCACHE            | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ VCACHE**](d3ddevinfo-vcache.md)                             | Retail/Debug | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| VERTEXSTATS       | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ D3DVERTEXSTATS**](d3ddevinfo-d3dvertexstats.md)             | Solo depuración   | [**Presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| VERTEXTIMINGS     | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9STAGETIMINGS**](d3ddevinfo-d3d9stagetimings.md)         | Retail/Debug | No procede                                              |



 

Algunas de las consultas requieren un evento de inicio y finalización, mientras que otras solo requieren un evento final. Las consultas que solo requieren un evento final comienzan cuando se produce otro evento implícito (que se muestra en la tabla). Todas las consultas devuelven una respuesta, excepto la consulta de eventos cuya respuesta es siempre **TRUE.** Una aplicación usa el estado de la consulta o el código de retorno de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).

## <a name="create-a-query"></a>Crear una consulta

Antes de crear una consulta, puede comprobar si el tiempo de ejecución admite consultas mediante una llamada a [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) con un **puntero NULL** como este:


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



Este método devuelve un código correcto si se puede crear una consulta; de lo contrario, devuelve un código de error. Una [**vez que CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) se realiza correctamente, puede crear un objeto de consulta como este:


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



Si esta llamada se realiza correctamente, se crea un objeto de consulta. La consulta está esencialmente inactiva en el estado señalado (con una respuesta sin inicializar) a la espera de ser emitida. Cuando haya terminado con la consulta, suélcela como cualquier otra interfaz.

## <a name="issue-a-query"></a>Emitir una consulta

Una aplicación cambia un estado de consulta mediante la emisión de una consulta. Este es un ejemplo de emisión de una consulta:


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



Una consulta en el estado señalado realizará una transición como esta cuando se emita:



| Tipo de problema                                | Transiciones de consulta a . . . |
|-------------------------------------------|--------------------------------|
| [**D3DISSUE \_ BEGIN**](d3dissue-begin.md) | Estado de la creación.                |
| [**D3DISSUE \_ END**](d3dissue-end.md)     | Estado emitido.                  |



 

Una consulta en el estado de creación realizará una transición como esta cuando se emita:



| Tipo de problema                                | Transiciones de consulta a . . .                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [**D3DISSUE \_ BEGIN**](d3dissue-begin.md) | (Sin transición, permanece en el estado de creación. Reinicia el corchete de consulta). |
| [**D3DISSUE \_ END**](d3dissue-end.md)     | Estado emitido.                                                             |



 

Una consulta en el estado emitido realizará una transición como esta cuando se emita:



| Tipo de problema                                | Transiciones de consulta a . . .                    |
|-------------------------------------------|---------------------------------------------------|
| [**D3DISSUE \_ BEGIN**](d3dissue-begin.md) | Estado de creación y reinicia el corchete de consulta.    |
| [**D3DISSUE \_ END**](d3dissue-end.md)     | Estado emitido después de abandonar la consulta existente. |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a>Comprobar el estado de la consulta y obtener la respuesta a la consulta

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) hace dos cosas:

1.  Devuelve el estado de consulta en el código de retorno.
2.  Devuelve la respuesta a la consulta en *pData*.

De cada uno de los tres estados de consulta, estos son los códigos de [**retorno de GetData:**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)



| Estado de la consulta | Código de retorno GetData |
|-------------|---------------------|
| Señalado    | S \_ OK               |
| Compilación    | Código de error          |
| Emitido      | S \_ FALSE            |



 

Por ejemplo, cuando una consulta está en el estado emitido y la respuesta a la consulta no está disponible, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) devuelve S \_ FALSE. Cuando el recurso finaliza su trabajo y la aplicación ha emitido un final de consulta, el recurso pasa la consulta al estado señalado. Desde el estado señalado, **GetData** devuelve S OK, lo que significa que la respuesta a la consulta \_ también se devuelve en *pData*. Por ejemplo, esta es la secuencia de eventos para devolver el número de píxeles dibujados en una secuencia de representación:

-   Crear la consulta.
-   Emita un evento de inicio.
-   Dibuje algo.
-   Emitir un evento final.

A continuación se muestra la secuencia de código correspondiente:


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

-   Llame [**a GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) para devolver el número de píxeles dibujados.
-   Especifique [**D3DGETDATA \_ FLUSH para**](d3dgetdata-flush.md) permitir que el recurso pueda realizar la transición de la consulta al estado señalado.
-   Sondee el recurso de consulta llamando a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) desde un bucle. Siempre que **GetData** devuelva S FALSE, significa \_ que el recurso aún no ha devuelto la respuesta.

El valor devuelto de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) indica básicamente en qué estado se encuentra la consulta. Los valores posibles son S \_ OK, S \_ FALSE y un error. No llame a **GetData** en una consulta que se encuentra en estado de creación.

-   S \_ OK significa que el recurso (GPU, controlador o runtime) ha finalizado. La consulta vuelve al estado señalado. [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)devuelve la respuesta (si existe).
-   S \_ FALSE significa que el recurso (GPU, controlador o tiempo de ejecución) todavía no puede devolver una respuesta. Esto podría deberse a que la GPU no ha finalizado o aún no ha visto el trabajo.
-   Un error significa que la consulta ha generado un error del que no se puede recuperar. Este podría ser el caso si el dispositivo se pierde durante una consulta. Una vez que una consulta ha generado un error (distinto de S FALSE), se debe volver a crear la consulta, lo que reiniciará la secuencia de consulta desde \_ el estado señalado.

En lugar de especificar [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md), que proporciona información más actualizada, podría proporcionar cero, que es una comprobación más ligera si la consulta está en el estado emitido. Si se proporciona cero, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) no vaciará el búfer de comandos. Por esta razón, debe tener cuidado para evitar bucles de infinación (consulte **GetData** para obtener más información). Dado que el tiempo de ejecución pone en cola el trabajo en el búfer de comandos, **D3DGETDATA \_ FLUSH** es un mecanismo para vaciar el búfer de comandos en el controlador (y, por lo tanto, la GPU; vea Generar perfiles precisos de llamadas API de [Direct3D (Direct3D 9).](accurately-profiling-direct3d-api-calls.md) Durante el vaciado del búfer de comandos, una consulta puede realizar la transición al estado señalado.

## <a name="example-an-event-query"></a>Ejemplo: una consulta de eventos

Una consulta de eventos no admite un evento begin.

-   Crear la consulta.
-   Emitir un evento final.
-   Sondee hasta que la GPU esté inactiva.
-   Emitir un evento final.


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



Esta es la secuencia de comandos que usa una consulta de eventos para generar perfiles de llamadas de la interfaz de programación de aplicaciones (API) (consulte Generación precisa de perfiles de llamadas a la API de [Direct3D (Direct3D 9).](accurately-profiling-direct3d-api-calls.md) Esta secuencia usa marcadores para ayudar a controlar la cantidad de trabajo en el búfer de comandos.

Tenga en cuenta que las aplicaciones deben prestar especial atención al gran costo asociado con el vaciado del búfer de comandos, ya que esto hace que el sistema operativo cambie al modo kernel, lo que incurrirá en una reducción de rendimiento importante. Las aplicaciones también deben ser conscientes de la pérdida de ciclos de CPU al esperar a que se completen las consultas.

Las consultas son una optimización que se usará durante la representación para aumentar el rendimiento. Por lo tanto, no es beneficioso dedicar tiempo a esperar a que finalice una consulta. Si se emite una consulta y los resultados aún no están listos en el momento en que la aplicación los comprueba, el intento de optimización no se ha hecho correctamente y la representación debe continuar con normalidad.

El ejemplo clásico de esto es durante la selección de oclusión. En lugar del **bucle while** anterior, una aplicación que usa consultas puede implementar la selección de oclusión para comprobar si una consulta ha finalizado en el momento en que necesita el resultado. Si la consulta no ha finalizado, continúe (como escenario en el peor de los casos) como si el objeto con el que se está probando no se haya ocluido (es decir, esté visible) y represente el objeto. El código tendría un aspecto similar al siguiente.


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

 

 
