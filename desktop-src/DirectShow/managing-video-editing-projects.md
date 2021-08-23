---
description: Administración de proyectos de edición de vídeo
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Administración de proyectos de edición de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe226f4fdc43889daac8e978086c67bd81c5d8d822902e7c041bf500f2836fb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584455"
---
# <a name="managing-video-editing-projects"></a>Administración de proyectos de edición de vídeo

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Las sugerencias siguientes le ayudarán a administrar proyectos [en DirectShow Editing Services](directshow-editing-services.md).

Cambios en la escala de tiempo

-   Si cambia la escala de tiempo después de compilar el gráfico de filtros, vuelva a llamar a [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) para volver a generar el front-end. Normalmente, esto no afecta al resto del gráfico. Sin embargo, en ocasiones, el motor de representación debe eliminar todo el gráfico antes de volver a generar el front-end. (Por ejemplo, esto sucede si agrega o quita un grupo). El **método ConnectFrontEnd** devuelve S \_ WARN \_ OUTPUTRESET para indicar que eliminó el gráfico. Si esto sucede, la aplicación debe recompilar la sección de representación del gráfico.
-   Para quitar todos los objetos completamente de la escala de tiempo, llame al [**método IAMTimeline::ClearAllGroups.**](iamtimeline-clearallgroups.md)

**Limpieza**

-   Cuando haya terminado de usar un motor de representación, llame al [**método IRenderEngine::ScrapIt.**](irenderengine-scrapit.md) Al igual que con cualquier objeto COM, asegúrese de liberar todos los punteros de interfaz cuando haya terminado de usarlo.
-   El motor de representación no mantiene un recuento de referencias en la escala de tiempo. No suelte la escala de tiempo antes de que haya terminado de usarlo y llame siempre a **ScrapIt en** el motor de representación en primer lugar.
-   Si libera todas las referencias a una escala de tiempo, no use ninguno de los objetos de esa escala de tiempo, aunque tenga recuentos de referencias en ellos.

**Varias instancias de escala de tiempo**

-   No mueva objetos de escala de tiempo entre escalas de tiempo. Cada objeto de una escala de tiempo debe crearse mediante esa escala de tiempo. La escala de tiempo contiene una memoria caché interna con información sobre los objetos que crea. mover objetos de escala de tiempo puede interrumpir la memoria caché.
-   Nunca use la misma instancia de un motor de representación con más de una escala de tiempo. El motor de representación contiene una memoria caché con información sobre la escala de tiempo. Varias escalas de tiempo interrumpirán la memoria caché y provocarán resultados impredecibles. Si necesita dos escalas de tiempo activas, cree instancias independientes de motores de representación para cada escala de tiempo.
-   Una escala de tiempo puede usar más de un motor de representación, pero no al mismo tiempo. Elimine el motor de representación anterior antes de usar otro motor de representación. (Normalmente lo haría al pasar de usar el motor de representación básico para la versión preliminar al motor de representación inteligente para la escritura de archivos).

**Persistencia**

-   El gráfico de filtros no es persistente cuando se guarda el proyecto en un archivo XML. Por lo tanto, perderá cualquier información relacionada con la recompresión inteligente, el formato de compresión o los parámetros de compresión. La aplicación debe restaurar estos parámetros después de cargar un proyecto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DirectShow Editing Services](using-directshow-editing-services.md)
</dt> </dl>

 

 



