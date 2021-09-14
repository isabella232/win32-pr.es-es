---
description: Cadenas de filtro
ms.assetid: c17b3b58-65ab-4e83-91f2-54a995f22ddf
title: Cadenas de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d22ee33f7bc24495bc5099d0abeca7b8c70bc6d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169978"
---
# <a name="filter-chains"></a>Cadenas de filtro

Una *cadena de filtros* es una secuencia de filtros que cumple las condiciones siguientes:

-   Cada filtro de la cadena tiene como máximo un pin de entrada conectado y un pin de salida conectado.
-   Es posible recorrer todos los filtros de la cadena sin atravesar filtros fuera de la cadena.

Por ejemplo, en el diagrama siguiente, los filtros A–B, C–D y F–G–H son cadenas de filtro. Cada subcadena de F–G–H (F–G y G–H) también es una cadena de filtros. Una cadena de filtros puede constar de un único filtro, por lo que los filtros A, B, C, D, F, G y H también son cadenas de filtro distintas. El filtro E tiene dos conexiones de entrada, por lo que cualquier secuencia de filtros que incluya el filtro E no es una cadena de filtros.

![cadena de filtros (ejemplo 1)](images/filter-chain1.png)

La [**interfaz IFilterChain proporciona**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain) los métodos siguientes para controlar las cadenas de filtro:



| Etiqueta | Value |
|---------------------------------------------------------------|---------------------------------|
| [**IFilterChain::StartChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-startchain)   | Inicia una cadena.                 |
| [**IFilterChain::StopChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-stopchain)     | Detiene una cadena.                  |
| [**IFilterChain::P auseChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-pausechain)   | Pausa una cadena.                 |
| [**IFilterChain::RemoveChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-removechain) | Quita una cadena del gráfico. |



 

No hay ningún método específico para agregar una cadena. Para agregar una cadena, inserte los nuevos filtros mediante el [**método IFilterGraph::AddFilter.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) A continuación, conecte los filtros mediante una llamada a [**IGraphBuilder::Conectar**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect), [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)o métodos similares.

Cuando se ejecuta el gráfico, una cadena de filtros puede cambiar entre en ejecución y detenido. Cuando el gráfico está en pausa, puede cambiar entre pausado y detenido. Estas son las únicas transiciones de estado posibles con cadenas de filtro.

## <a name="filter-chain-guidelines"></a>Directrices de la cadena de filtros

Cuando se usan **métodos IFilterChain,** es importante asegurarse de que los filtros del gráfico pueden admitir operaciones de encadenamiento de filtros. De lo contrario, podría provocar interbloqueos o errores de grafo. Los filtros conectados a la cadena deben funcionar correctamente después de que la cadena cambie de estado.

La mejor manera de usar **IFilterChain** es con un conjunto de filtros que ha diseñado específicamente para el encadenamiento. Use las siguientes directrices para asegurarse de que los filtros son seguros para las operaciones de cadena de filtros. Estos puntos hacen referencia al diagrama siguiente.

![cadena de filtros (ejemplo 2)](images/filter-chain2.png)

-   Antes de que cambie el estado de la cadena de filtros, se deben completar todas las llamadas de procesamiento de datos en el límite de la cadena de filtros. Esta regla se aplica a los métodos [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)e [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream). Los filtros de la cadena deben devolver de las llamadas a estos métodos realizadas por filtros fuera de la cadena; y los filtros fuera de la cadena deben devolverse de las llamadas realizadas por filtros dentro de la cadena.

Por ejemplo, en el diagrama anterior, el filtro B debe completar las llamadas de procesamiento de datos del filtro A y el filtro E debe finalizar las llamadas del filtro D. Si los pins exponen las interfaces [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) e [**IPinConnection,**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) puede insertar los datos a través del gráfico llamando a los métodos [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) e [**IGraphConfig::P ushThroughData,**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) como se describe en Reconexión [dinámica.](dynamic-reconnection.md) Los filtros también pueden admitir métodos privados para insertar los datos.

-   Los filtros ascendentes deben esperar que cambie el estado de la cadena. Por ejemplo, en el diagrama anterior, suponga que la cadena está detenida, pero filtre A llama a **IMemInputPin::Receive.** Se produce un error en la llamada y la respuesta del filtro A es detener el streaming. Cuando la aplicación reinicia la cadena, no tiene ningún efecto porque el filtro A ya no transmite datos.
-   Los filtros de nivel inferior también deben esperar que cambie el estado de la cadena. Si no es así, el filtro de nivel inferior podría bloquearse mientras espera muestras que nunca llegan. Por ejemplo, los filtros de multiplexor (MUX) a menudo requieren datos de todos sus pines de entrada. Detener el flujo de datos de un pin de entrada podría bloquear el procesamiento de las otras secuencias. Esto puede hacer que el gráfico interbloquee.
-   Cada conexión de pin de un filtro fuera de la cadena a un filtro dentro de la cadena debe tener su propio asignador, que no comparten otras conexiones. Cuando la cadena cambia de estado o se quita del gráfico, es posible que se desasigne el asignador. Si otras conexiones usaban el mismo asignador, ya no pueden procesar ejemplos.
-   No quite una cadena a menos que los filtros conectados a la cadena admitan la desconexión dinámica. Normalmente, los filtros conectados admitirán la **interfaz IPinConnection** o **IPinFlowControl,** pero podrían admitir interfaces privadas en su lugar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dynamic Graph Building](dynamic-graph-building.md)
</dt> </dl>

 

 



