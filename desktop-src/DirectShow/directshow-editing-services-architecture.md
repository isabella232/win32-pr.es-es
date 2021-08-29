---
description: DirectShow Arquitectura de servicios de edición
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: DirectShow Arquitectura de servicios de edición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add81e579b89c0053e5833aab67d84e942a111c90df2e2b665531c507f7be1e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966695"
---
# <a name="directshow-editing-services-architecture"></a>DirectShow Arquitectura de servicios de edición

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En la ilustración siguiente se muestra la arquitectura [de DirectShow Editing Services](directshow-editing-services.md) (DES).

![arquitectura de servicios de edición de directshow](images/architecture.png)

-   Escala de tiempo: representa una producción de vídeo como una colección de clips, transiciones y efectos de origen, organizados en un conjunto de pistas anidadas. Para obtener más información, vea [El modelo de escala de tiempo](the-timeline-model.md).
-   Analizador XML: analiza la escala de tiempo y genera un archivo de salida, o lee un archivo de entrada y genera una escala de tiempo. DES admite un formato de persistencia basado en XML.
-   Motor de representación: convierte la escala de tiempo en un formulario que se puede representar como medio de streaming. De forma predeterminada, el motor de representación genera un DirectShow gráfico de filtro (consulte la sección siguiente).
-   Localizador de medios: mantiene una caché de ubicaciones de elementos multimedia. Cuando se produce un error al intentar abrir un elemento multimedia, DES usa la memoria caché para buscar el elemento, en función de un historial de aperturas correctas.

La escala de tiempo es una descripción abstracta de un proyecto de edición de vídeo. Especifica los clips de origen usados en el proyecto, las horas de inicio y de detenerse, los efectos y las transiciones, etc. Sin embargo, la escala de tiempo no representa las secuencias de audio y vídeo. En su lugar, el motor de representación convierte la escala de tiempo en un gráfico de filtros, ya sea para la vista previa o la salida del archivo. Una aplicación manipula la escala de tiempo en lugar de manipular directamente el gráfico de filtros, lo que sería complicado y propenso a errores.

En la tabla siguiente se enumeran las tareas principales que realiza una aplicación de edición de vídeo típica, junto con las interfaces que admiten cada tarea. En las secciones posteriores se describen estas tareas y las interfaces con más detalle.



| Tarea                                     | Interfaces                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| Construir o modificar una escala de tiempo.          | [**IAMTimeline**](iamtimeline.md) y las otras interfaces **IAMTimelineXXXX**          |
| Guarde y cargue los archivos del proyecto.             | [**IXml2Dex**](ixml2dex.md)                                                             |
| Obtenga una vista previa de un proyecto o escríbalo en un archivo. | [**IRenderEngine**](irenderengine.md), [ **ISmartRenderEngine**](ismartrenderengine.md) |



 

Además, una aplicación puede realizar algunas o todas las tareas secundarias siguientes.



| Tarea                                                                                           | Interfaces                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| Obtenga información sobre los archivos multimedia. (Número de secuencias; formato y duración de cada secuencia). | [**IMediaDet**](imediadet.md)                                               |
| Establecer propiedades en transiciones y efectos.                                                     | [**IPropertySetter**](ipropertysetter.md)                                   |
| Reciba una notificación cuando se produzcan errores durante la representación.                                       | [**IAMSetErrorLog**](iamseterrorlog.md), [ **IAMErrorLog**](iamerrorlog.md) |
| Recuperar fotogramas de póster.                                                                        | [**IMediaDet**](imediadet.md), [ **ISampleGrabber**](isamplegrabber.md)     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas iniciales con DirectShow Editing Services](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



