---
description: Administrar proyectos de edición de vídeo
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Administrar proyectos de edición de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666111"
---
# <a name="managing-video-editing-projects"></a>Administrar proyectos de edición de vídeo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Las siguientes sugerencias le ayudarán a administrar los proyectos de los [servicios de edición de DirectShow](directshow-editing-services.md).

Cambios en la escala de tiempo

-   Si cambia la escala de tiempo después de compilar el gráfico de filtros, llame de nuevo a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para recompilar el front-end. Normalmente, esto no afecta al resto del gráfico. Sin embargo, en ocasiones, el motor de representación debe eliminar todo el gráfico antes de recompilar el front-end. (Por ejemplo, esto sucede si agrega o quita un grupo). El método **ConnectFrontEnd** devuelve S \_ WARN \_ OUTPUTRESET para indicar que ha eliminado el gráfico. Si esto ocurre, la aplicación debe volver a generar la sección de representación del gráfico.
-   Para quitar todos los objetos completamente de la escala de tiempo, llame al método [**IAMTimeline:: ClearAllGroups**](iamtimeline-clearallgroups.md) .

**Limpieza**

-   Cuando haya terminado de usar un motor de representación, llame al método [**IRenderEngine:: ScrapIt**](irenderengine-scrapit.md) . Al igual que con cualquier objeto COM, asegúrese de liberar todos los punteros de interfaz cuando haya terminado de usarlo.
-   El motor de representación no mantiene un recuento de referencias en la escala de tiempo. No libere la escala de tiempo antes de que haya terminado de usarla y llame primero a **ScrapIt** en el motor de representación.
-   Si libera todas las referencias a una escala de tiempo, no utilice ninguno de los objetos de esa escala de tiempo, incluso si contiene recuentos de referencias en ellos.

**Varias instancias de escala de tiempo**

-   No mueva los objetos Timeline entre las escalas de tiempo. Cada objeto de una escala de tiempo debe crearse en esa escala de tiempo. La escala de tiempo contiene una memoria caché interna con información sobre los objetos que crea; mover objetos de escala de tiempo puede interrumpir la memoria caché.
-   Nunca utilice la misma instancia de un motor de representación con más de una escala de tiempo. El motor de representación contiene una memoria caché con información sobre la escala de tiempo. Varias escalas de tiempo interrumpirán la memoria caché y provocarán resultados imprevisibles. Si necesita dos escalas de tiempo activas, cree instancias independientes de motores de representación para cada escala de tiempo.
-   Una escala de tiempo puede usar más de un motor de representación, pero no al mismo tiempo. Elimine el antiguo motor de representación antes de usar otro motor de representación. (Normalmente, esto se haría al pasar de usar el motor de representación básico para la vista previa al motor de representación inteligente para la escritura de archivos).

**Persistencia**

-   El gráfico de filtro no es persistente cuando guarda el proyecto en un archivo XML. Por lo tanto, se pierde toda la información relacionada con la recompresión inteligente, el formato de compresión o los parámetros de compresión. Depende de la aplicación restaurar estos parámetros después de cargar un proyecto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar servicios de edición de DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



