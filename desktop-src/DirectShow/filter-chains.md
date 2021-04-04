---
description: Cadenas de filtro
ms.assetid: c17b3b58-65ab-4e83-91f2-54a995f22ddf
title: Cadenas de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46e374aca71b024773e4177d09e67c7ee6034ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906757"
---
# <a name="filter-chains"></a>Cadenas de filtro

Una *cadena* de filtros es una secuencia de filtros que cumple las condiciones siguientes:

-   Cada filtro de la cadena tiene como máximo un PIN de entrada conectado y un PIN de salida conectado.
-   Es posible atravesar todos los filtros de la cadena sin atravesar los filtros fuera de la cadena.

Por ejemplo, en el diagrama siguiente, los filtros A – B, C – D y F – G – H son cadenas de filtro. Cada subcadena de F – G – H (F – G y G – H) también es una cadena de filtros. Una cadena de filtros puede constar de un solo filtro, por lo que los filtros A, B, C, D, F, G y H también son cadenas de filtro diferentes. El filtro E tiene dos conexiones de entrada, por lo que cualquier secuencia de filtros que incluya el filtro E no es una cadena de filtros.

![cadena de filtros (ejemplo 1)](images/filter-chain1.png)

La interfaz [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain) proporciona los siguientes métodos para controlar las cadenas de filtro:



|                                                               |                                 |
|---------------------------------------------------------------|---------------------------------|
| [**IFilterChain::StartChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-startchain)   | Inicia una cadena.                 |
| [**IFilterChain::StopChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-stopchain)     | Detiene una cadena.                  |
| [**IFilterChain::P auseChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-pausechain)   | Pausa una cadena.                 |
| [**IFilterChain::RemoveChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-removechain) | Quita una cadena del gráfico. |



 

No hay ningún método específico para agregar una cadena. Para agregar una cadena, inserte los nuevos filtros mediante el método [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . A continuación, conecte los filtros mediante una llamada a [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect), [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)o métodos similares.

Cuando se está ejecutando el gráfico, una cadena de filtros puede cambiar entre ejecución y detenida. Cuando el gráfico está en pausa, puede cambiar entre pausado y detenido. Estas son las únicas transiciones de estado posibles con las cadenas de filtro.

## <a name="filter-chain-guidelines"></a>Instrucciones de la cadena de filtros

Cuando se usan métodos **IFilterChain** , es importante asegurarse de que los filtros del gráfico pueden admitir operaciones de encadenamiento de filtros. De lo contrario, podría causar interbloqueos o errores de grafo. Los filtros conectados a la cadena deben funcionar correctamente después de que cambie el estado de la cadena.

La mejor manera de usar **IFilterChain** es con un conjunto de filtros que se han diseñado específicamente para el encadenamiento. Utilice las siguientes directrices para asegurarse de que los filtros son seguros para las operaciones de cadena de filtros. Estos puntos hacen referencia al diagrama siguiente.

![cadena de filtros (ejemplo 2)](images/filter-chain2.png)

-   Antes de que cambie el estado de la cadena de filtros, se deben completar todas las llamadas de procesamiento de datos en el límite de la cadena de filtros. Esta regla se aplica a los métodos [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)y [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream). Los filtros de la cadena deben devolver de las llamadas a estos métodos realizados por filtros fuera de la cadena. y los filtros fuera de la cadena deben devolver desde las llamadas realizadas por filtros dentro de la cadena.

Por ejemplo, en el diagrama anterior, el filtro B debe completar cualquier llamada de procesamiento de datos del filtro A y el filtro E debe finalizar cualquier llamada del filtro D. Si los pin exponen las interfaces [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) y [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) , puede enviar los datos a través del gráfico mediante una llamada a los métodos [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) y [**IGraphConfig::P ushthroughdata**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) , como se describe en [reconexión dinámica](dynamic-reconnection.md). Los filtros también pueden admitir métodos privados para insertar los datos.

-   Los filtros ascendentes deben esperar que el estado de la cadena cambie. Por ejemplo, en el diagrama anterior, supongamos que la cadena está detenida pero el filtro A llama a **IMemInputPin:: Receive**. Se produce un error en la llamada y la respuesta del filtro a es detener el streaming. Cuando la aplicación reinicia la cadena, no tiene ningún efecto porque el filtro A ya no transmite datos.
-   Los filtros de nivel inferior también deben esperar que el estado de la cadena cambie. Si no es así, el filtro de nivel inferior podría bloquearse mientras espera las muestras que nunca llegan. Por ejemplo, los filtros del multiplexor (MUX) suelen requerir datos de todos los pin de entrada. Detener el flujo de datos de un PIN de entrada podría impedir que se procesen los demás flujos. Esto puede hacer que el gráfico se interbloquee.
-   Cada conexión de PIN de un filtro fuera de la cadena a un filtro dentro de la cadena debe tener su propio asignador, que no se comparte con otras conexiones. Cuando la cadena cambia de estado o se quita del gráfico, es posible que el asignador esté desasignado. Si otras conexiones usaban el mismo asignador, ya no podrán procesar ejemplos.
-   No quite una cadena a menos que los filtros conectados a la cadena admitan la desconexión dinámica. Normalmente, los filtros conectados admitirán la interfaz **IPinConnection** o **IPinFlowControl** , pero podrían admitir interfaces privadas en su lugar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de gráficos dinámicos](dynamic-graph-building.md)
</dt> </dl>

 

 



