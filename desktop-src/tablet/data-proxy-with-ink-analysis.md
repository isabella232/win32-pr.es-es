---
description: Como se mencionó en Información general sobre análisis de lápiz, la tecnología de análisis de entrada de lápiz mantiene internamente un modelo de documento basado en árbol para contener los resultados de análisis y las relaciones.
ms.assetid: 33ba9292-3bc7-41ba-a602-e2fc94cd3a57
title: Proxy de datos con análisis de entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad79a37a3220351adad56c0a131392e96964714114ba1e0a982833b07bc85077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092784"
---
# <a name="data-proxy-with-ink-analysis"></a>Proxy de datos con análisis de entrada de lápiz

Como se mencionó en [Información general sobre análisis](ink-analysis-overview.md)de entrada de lápiz, la tecnología de análisis de entrada de lápiz mantiene internamente un modelo de documento basado en árbol para contener los resultados de análisis y las relaciones. Si la aplicación ya tiene un almacén de documentos establecido que es diferente, deberá usar las características de análisis de entrada de lápiz diseñadas para proxy de datos entre modelos de documento dispares.

## <a name="types-of-data-proxy"></a>Tipos de proxy de datos

Las características de proxy de datos permiten a la aplicación:

-   Integre los datos de resultados de análisis de nuevo en un modelo de documento existente.
-   Vuelva a comunicar los resultados anteriores (o estado) en [**InkAnalyzer.**](inkanalyzer.md)
-   Comunique el estado que no es de entrada de lápiz en [**InkAnalyzer.**](inkanalyzer.md)
-   Comunique solo el conjunto mínimo de datos (estado anterior y sin entrada de lápiz) necesario para completar la operación de análisis.
-   Actualice fácilmente el modelo de documento de aplicación interno con resultados de análisis.

Hay dos enfoques básicos para el proxy de datos de análisis de entrada de lápiz. Las diferencias se producen en los detalles de cuándo y cómo se produce la sincronización entre los modelos de documento. El primer enfoque, la actualización sincrónica, requiere la modificación del modelo de documento de análisis de lápiz a medida que se producen cambios en el documento de aplicación. El segundo enfoque, la actualización a petición, solo requiere que los datos afectados por los cambios en el modelo de documento de aplicación se pasen a [**InkAnalyzer**](inkanalyzer.md). Es decir, solo se deben pasar a **InkAnalyzer** los datos de las partes del modelo de documento análisis de lápiz que se encuentran en la misma área que las modificaciones en el documento de aplicación, ya que los necesita.

### <a name="synchronous-update"></a>Actualización sincrónica

El enfoque de actualización sincrónica requiere la modificación (creación y eliminación) de nodos en la colección de objetos [**ContextNode**](icontextnode.md) del objeto [**InkAnalyzer**](inkanalyzer.md) a medida que se producen en el documento de aplicación. Por ejemplo, cada vez que se agrega una palabra de texto a la aplicación, se crea un **contextNode** con estilo **TextWord** correspondiente en **InkAnalyzer**. Si cambia la ubicación de la palabra de texto en la página, la ubicación del **ContextNode** correspondiente se actualiza al mismo tiempo. Este método es menos eficaz en términos de recursos informáticos que el método a petición porque cada cambio de documento implica una actualización de **InkAnalyzer,** incluso si el cambio no afecta a la entrada de lápiz que se está analizando.

El ejemplo siguiente está pensado para mostrar cómo funciona la actualización sincrónica. Imagine una aplicación que tiene un modelo de documento existente. Cuando el usuario final realiza un cambio en el documento, como agregar texto nuevo, el cambio se procesa de la manera siguiente:

1.  El usuario final crea los nuevos datos.
2.  La aplicación determina cómo procesar los datos, los almacena y los representa.
3.  Para fines prácticos, los siguientes pasos se llevan a cabo simultáneamente.
    1.  La aplicación coloca los datos en su modelo de documento.
    2.  La aplicación crea un [**InkAnalyzer y**](inkanalyzer.md) lo actualiza. Esto garantiza simultáneamente que **InkAnalyzer** siempre tiene la información más reciente.
    3.  La aplicación llama [**a BackgroundAnalyze en**](iinkanalyzer-backgroundanalyze.md) [**InkAnalyzer para**](inkanalyzer.md) iniciar el análisis.
4.  Se desencadena una serie de eventos si el cambio implica entrada de lápiz y [**InkAnalyzer**](inkanalyzer.md) determina nuevos resultados. Se desencadena un evento por cada cambio realizado en la colección de objetos [**ContextNode**](icontextnode.md) en **InkAnalyzer.** Estos eventos incluyen [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md), [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md), [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md), [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)y [**ContextNodeReparenting.**](-ianalysisproxyevents-contextnodereparenting.md) La aplicación controla estos eventos para proxy los resultados de la operación de análisis de nuevo en el modelo de documento según corresponda.
5.  La aplicación actualiza el diseño del documento, extracndo los nuevos datos del modelo de documento.
6.  Los nuevos datos se representan de nuevo al usuario final.

### <a name="on-demand-update"></a>Actualización a petición

El enfoque a petición solo requiere que se pasen los datos para los objetos [**ContextNode**](icontextnode.md) que se encuentran en las áreas que se están analizando. Los objetos **ContextNode necesarios** se extraen del modelo de documentos de la aplicación justo después de invocar la operación de análisis y, de nuevo, justo antes de conciliar los resultados. Aunque es más complicado de implementar que las actualizaciones sincrónicas, este enfoque produce mejores resultados de rendimiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre análisis de entrada de lápiz](ink-analysis-overview.md)
</dt> <dt>

[**InkAnalyzer (Clase, C++)**](inkanalyzer.md)
</dt> <dt>

[**Microsoft.Ink.InkAnalyzer**](/previous-versions/ms583671(v=vs.100))
</dt> <dt>

[**Microsoft.Ink.ContextNode**](/previous-versions/ms551996(v=vs.100))
</dt> </dl>

 

 
