---
description: Arquitectura de servicios de edición de DirectShow
ms.assetid: ba6cc3f1-9130-4197-8501-c2d0a088e847
title: Arquitectura de servicios de edición de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6059eebe9228e61d3de9677972eedfcb51c62
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105652311"
---
# <a name="directshow-editing-services-architecture"></a>Arquitectura de servicios de edición de DirectShow

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En la ilustración siguiente se muestra la arquitectura de los [servicios de edición de DirectShow](directshow-editing-services.md) (des).

![arquitectura de servicios de edición de DirectShow](images/architecture.png)

-   Timeline: representa una producción de vídeo como una colección de clips, transiciones y efectos de origen, organizada en un conjunto de pistas anidadas. Para obtener más información, vea [el modelo Timeline](the-timeline-model.md).
-   Analizador XML: analiza la escala de tiempo y genera un archivo de salida, o lee un archivo de entrada y genera una escala de tiempo. DES admite un formato de persistencia basado en XML.
-   Motor de representación: traduce la escala de tiempo a un formato que se puede representar como un medio de streaming. De forma predeterminada, el motor de representación genera un gráfico de filtros de DirectShow (consulte la sección siguiente).
-   Localizador de medios: mantiene una memoria caché de las ubicaciones de los elementos multimedia. Cuando se produce un error al intentar abrir un elemento multimedia, DES usa la memoria caché para buscar el elemento, en función de un historial de aperturas correctas.

La escala de tiempo es una descripción abstracta de un proyecto de edición de vídeo. Especifica los clips de origen usados en el proyecto, las horas de inicio y de finalización, los efectos y las transiciones, etc. Sin embargo, la escala de tiempo no representa las secuencias de audio y vídeo. En su lugar, el motor de representación traduce la escala de tiempo en un gráfico de filtros, para la vista previa o la salida del archivo. Una aplicación manipula la escala de tiempo en lugar de manipular directamente el gráfico de filtro, lo que sería engorroso y propenso a errores.

En la tabla siguiente se enumeran las tareas principales que realiza una aplicación de edición de vídeo típica, junto con las interfaces que admiten cada tarea. En secciones posteriores se describen con más detalle estas tareas y las interfaces.



| Tarea                                     | Interfaz (s)                                                                             |
|------------------------------------------|------------------------------------------------------------------------------------------|
| Construya o modifique una escala de tiempo.          | [**IAMTimeline**](iamtimeline.md) y las otras interfaces de **IAMTimelineXXXX**          |
| Guardar y cargar archivos de proyecto.             | [**IXml2Dex**](ixml2dex.md)                                                             |
| Obtenga una vista previa de un proyecto o escríbalo en un archivo. | [**IRenderEngine**](irenderengine.md), [ **ISmartRenderEngine**](ismartrenderengine.md) |



 

Además, una aplicación puede realizar algunas o todas las tareas secundarias siguientes.



| Tarea                                                                                           | Interfaz (s)                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| Obtener información acerca de los archivos multimedia. (Número de secuencias; formato y duración de cada secuencia). | [**IMediaDet**](imediadet.md)                                               |
| Establezca las propiedades en las transiciones y los efectos.                                                     | [**IPropertySetter**](ipropertysetter.md)                                   |
| Recibir una notificación cuando se produzcan errores durante la representación.                                       | [**IAMSetErrorLog**](iamseterrorlog.md), [ **IAMErrorLog**](iamerrorlog.md) |
| Recuperar fotogramas de póster.                                                                        | [**IMediaDet**](imediadet.md), [ **ISampleGrabber**](isamplegrabber.md)     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción con servicios de edición de DirectShow](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



