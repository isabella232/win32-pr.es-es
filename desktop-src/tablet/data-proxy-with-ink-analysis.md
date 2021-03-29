---
description: Como se mencionó en información general de análisis de tinta, la tecnología de análisis de tinta mantiene internamente un modelo de documento basado en árbol para contener los resultados del análisis y las relaciones.
ms.assetid: 33ba9292-3bc7-41ba-a602-e2fc94cd3a57
title: Proxy de datos con análisis de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52717b955625e67f50c20703dd0e84449aa1037f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912917"
---
# <a name="data-proxy-with-ink-analysis"></a>Proxy de datos con análisis de tinta

Como se mencionó en [información general de análisis de tinta](ink-analysis-overview.md), la tecnología de análisis de tinta mantiene internamente un modelo de documento basado en árbol para contener los resultados del análisis y las relaciones. Si su aplicación ya tiene un almacén de documentos establecido que es diferente, deberá usar las características de análisis de tinta diseñadas para obtener datos de proxy entre modelos de documento dispares.

## <a name="types-of-data-proxy"></a>Tipos de proxy de datos

Las características del proxy de datos permiten a la aplicación:

-   Integre los datos de los resultados del análisis de nuevo en un modelo de documento existente.
-   Comunicar los resultados anteriores (o el estado) al [**InkAnalyzer**](inkanalyzer.md).
-   Comunicar el estado sin tinta en el [**InkAnalyzer**](inkanalyzer.md).
-   Comunicar solo el conjunto mínimo de datos (estado anterior y sin tinta) necesario para completar la operación de análisis.
-   Actualice fácilmente el modelo de documento de aplicación interno con los resultados del análisis.

Hay dos enfoques básicos para el proxy de datos de análisis de tinta. Las diferencias se establecen en los detalles de Cuándo y cómo se produce la sincronización entre los modelos de documento. El primer enfoque, la actualización sincrónica, requiere la modificación del modelo de documento de análisis de tinta cuando se producen cambios en el documento de la aplicación. El segundo enfoque, la actualización a petición, solo requiere los datos afectados por los cambios en el modelo de documento de aplicación que se van a pasar a [**InkAnalyzer**](inkanalyzer.md). Es decir, solo los datos de las partes del modelo de documento de análisis de tinta que se encuentran en la misma área que las modificaciones en el documento de la aplicación se deben pasar al **InkAnalyzer** a medida que los necesite.

### <a name="synchronous-update"></a>Actualización sincrónica

El enfoque de actualización sincrónica requiere la modificación (creación y eliminación) de los nodos de la colección del objeto [**InkAnalyzer**](inkanalyzer.md) de los objetos [**ContextNode**](icontextnode.md) cuando se producen en el documento de la aplicación. Por ejemplo, cada vez que se agrega una palabra de texto a la aplicación, se crea una **ContextNode** de estilo **TextWord** correspondiente en el **InkAnalyzer**. Si cambia la ubicación de la palabra de texto en la página, la ubicación del **ContextNode** correspondiente se actualiza al mismo tiempo. Este método es menos eficaz en cuanto a recursos informáticos que el método a petición porque cada cambio de documento implica una actualización de **InkAnalyzer**, incluso si el cambio no afecta a la entrada de lápiz que se está analizando.

El ejemplo siguiente está pensado para mostrar cómo funciona la actualización sincrónica. Imagine una aplicación que tiene un modelo de documento existente. Cuando el usuario final realiza un cambio en el documento, como agregar texto nuevo, el cambio se procesa de la siguiente manera:

1.  El usuario final crea los datos nuevos.
2.  La aplicación determina cómo procesar los datos, los almacena y los representa.
3.  A efectos prácticos, se llevan a cabo los siguientes pasos simultáneamente.
    1.  La aplicación coloca los datos en su modelo de documento.
    2.  La aplicación crea un [**InkAnalyzer**](inkanalyzer.md) y lo actualiza. De esta forma, se garantiza que el **InkAnalyzer** siempre tiene la información más reciente.
    3.  La aplicación llama a [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) en [**InkAnalyzer**](inkanalyzer.md) para comenzar el análisis.
4.  Se desencadena una serie de eventos si el cambio implica tinta y el [**InkAnalyzer**](inkanalyzer.md) determina los nuevos resultados. Se desencadena un evento para cada cambio realizado en la colección de objetos [**ContextNode**](icontextnode.md) en **InkAnalyzer**. Estos eventos incluyen [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md), [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md), [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md), [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)y [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md). La aplicación controla estos eventos para volver a obtener el proxy de los resultados de la operación de análisis en el modelo de documento según corresponda.
5.  La aplicación actualiza el diseño del documento, extrayendo los datos nuevos del modelo de documento.
6.  Los nuevos datos se representarán al usuario final.

### <a name="on-demand-update"></a>Actualización a petición

El enfoque a petición solo requiere que los datos se pasen para los objetos [**ContextNode**](icontextnode.md) que se encuentran en las áreas que se están analizando. Los objetos **ContextNode** necesarios se extraen del modelo de documento de la aplicación justo después de invocar la operación de análisis y de nuevo justo antes de reconciliar los resultados. Aunque es más complicado implementar que las actualizaciones sincrónicas, este enfoque produce mejores resultados de rendimiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de análisis de tinta](ink-analysis-overview.md)
</dt> <dt>

[**InkAnalyzer (clase) (C++)**](inkanalyzer.md)
</dt> <dt>

[**Microsoft. Ink. InkAnalyzer**](/previous-versions/ms583671(v=vs.100))
</dt> <dt>

[**Microsoft. Ink. ContextNode**](/previous-versions/ms551996(v=vs.100))
</dt> </dl>

 

 
