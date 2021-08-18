---
title: Uso de WinSAT
description: Puede usar la API de Windows System Assessment Tool (WinSAT) para iniciar evaluaciones formales y ad hoc de la configuración de hardware del equipo, recuperar la puntuación base del equipo y las puntuaciones de cada subcomponente de la evaluación y recuperar detalles de la evaluación, como los detalles del procesador que se evaluó.
ms.assetid: b0860c4a-cec3-440c-b31a-7e7ad1b393d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23cf26d31ccbd3eb6e51fb1717c055fb6538c57612d374b0a3b7a2a5b2382681
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733791"
---
# <a name="using-winsat"></a>Uso de WinSAT

\[WinSAT puede modificarse o no estar disponible para las versiones después de Windows 8.1.\]

Puede usar la API de Windows System Assessment Tool (WinSAT) para iniciar evaluaciones [formales](#initiating-an-assessment) y ad hoc de la configuración de hardware del equipo, recuperar la puntuación [base](#retrieving-the-scores-of-the-assessment) del equipo y las puntuaciones de cada subcomponente de la evaluación y recuperar detalles de la [evaluación,](#retrieving-details-of-the-assessment)como los detalles del procesador que se evaluó.

## <a name="initiating-an-assessment"></a>Inicio de una evaluación

Después Windows 8.1 puede iniciar evaluaciones formales y ad hoc del equipo. Una evaluación formal evalúa los siguientes subcomponentes del equipo:

-   CPU
-   Memoria
-   Disco primario
-   Tarjeta de vídeo

Para iniciar una evaluación formal, llame al método [**IInitiateWinSATAssessment::InitiateFormalAssessment.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment) Los resultados de las evaluaciones formales se guardan en el almacén de evaluación y se pueden recuperar en una fecha posterior.

Normalmente, se usan evaluaciones ad hoc para evaluar solo un subcomponente del equipo, por ejemplo, la CPU o la memoria. Sin embargo, puede usar el **modificador formal** para evaluar todos los subcomponentes. Para iniciar una evaluación ad hoc, llame al método [**IInitiateWinSATAssessment::InitiateAssessment.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment) Tenga en cuenta que los resultados de las evaluaciones ad hoc no se guardan en el almacén de evaluación.

Para recuperar la notificación cuando se realiza el progreso o cuando se completa la evaluación, implemente la [**interfaz IWinSATInitiateEvents.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iwinsatinitiateevents)

No se pueden ejecutar evaluaciones formales de forma remota o en un equipo que se ejecuta con baterías. Tampoco puede ejecutar de forma remota una evaluación ad hoc en el subcomponente de gráficos.

## <a name="retrieving-the-scores-of-the-assessment"></a>Recuperación de las puntuaciones de la evaluación

Puede recuperar la puntuación base del equipo y la puntuación de cada subcomponente de la evaluación. Puede usar la API para recuperar las puntuaciones solo para las evaluaciones formales. Para recuperar las puntuaciones de las evaluaciones ad hoc, debe incluir el argumento **-xml** en la línea de comandos para guardar los resultados de la evaluación en un archivo XML y, a continuación, analizar el archivo para la puntuación del subcomponente.

La puntuación base es una medida general de la configuración de hardware del equipo. Por lo general, una puntuación base mayor significa que el equipo tendrá un rendimiento mejor y más rápido que un equipo con una puntuación base inferior, especialmente cuando se realizan tareas más avanzadas y que consumen muchos recursos.

Cada componente de hardware recibe una puntuación individual. La puntuación total del equipo viene determinada por la puntuación inferior. Por ejemplo, si la puntuación inferior de un componente de hardware individual es 2.6, la puntuación total será 2.6. La puntuación total no es la media de puntuaciones combinadas.

Un usuario puede usar la puntuación base para comprar programas y otro software que coincidan con la puntuación base de su equipo. Por ejemplo, si el equipo tiene una puntuación base de 3,3, el usuario puede comprar con confianza cualquier software diseñado para esta versión de Windows que requiera un equipo con una puntuación base de 3 o inferior.

Para recuperar la puntuación base, primero llame al método [**IQueryRecentWinSATAssessment::get \_ Info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) para obtener la interfaz [**IProvideWinSATResultsInfo.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) A continuación, llame [**al método IProvideWinSATResultsInfo::get \_ SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) para obtener la puntuación base.

Un usuario puede usar puntuaciones de subcomponentes para determinar si un subcomponente del equipo puede admitir un tipo específico de aplicación. Por ejemplo, un usuario que dedica más tiempo a leer o escribir documentos puede requerir una puntuación más alta para el disco que un usuario que ejecuta aplicaciones científicas, y un usuario que ejecuta aplicaciones científicas probablemente querrá una puntuación de subcomponentes de CPU más alta y puede no preocuparse por una puntuación de disco inferior.

Para recuperar la puntuación de cada subcomponente, primero llame al método [**IQueryRecentWinSATAssessment::get \_ Info**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_info) para obtener la interfaz [**IProvideWinSATResultsInfo.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatresultsinfo) A continuación, llame al método [**IProvideWinSATResultsInfo::GetAssessmentInfo**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-getassessmentinfo) para obtener la interfaz [**IProvideWinSATAssessmentInfo.**](/windows/desktop/api/Winsatcominterfacei/nn-winsatcominterfacei-iprovidewinsatassessmentinfo) Para cada subcomponente cuya puntuación desea recuperar, llame al método [**IProvideWinSATAssessmentInfo::get \_ Score.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score)

## <a name="retrieving-details-of-the-assessment"></a>Recuperación de los detalles de la evaluación

La API de WinSAT proporciona la puntuación base general y las puntuaciones de cada subcomponente. Para obtener detalles de la evaluación (por ejemplo, las métricas usadas para calcular la puntuación y los detalles del procesador que se evaluó), debe recuperar los datos del documento de evaluación XML. Para recuperar los detalles de la evaluación formal más reciente, llame al método [**\_ XML IQueryRecentWinSATAssessment::get.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryrecentwinsatassessment-get_xml) Para recuperar los detalles de cada evaluación del almacén de datos winSAT, llame al método [**IQueryAllWinSATAssessments::get \_ AllXML.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iqueryallwinsatassessments-get_allxml)

Para obtener información sobre el esquema XML y los detalles que puede recuperar, vea [Esquema WinSAT](winsat-schema.md).

 

 




