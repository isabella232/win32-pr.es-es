---
description: 'Hay cuatro niveles en la biblioteca de análisis de tinta: Windows Forms, WPF, COM y el nivel base. En esta sección se describe el uso de cada capa.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Uso de la API de análisis de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000977"
---
# <a name="ink-analysis-api-usage"></a>Uso de la API de análisis de tinta

Hay cuatro niveles en la biblioteca de análisis de tinta: Windows Forms, WPF, COM y el nivel base. En esta sección se describe el uso de cada capa.

## <a name="ink-analysis-api-overview"></a>Introducción a Ink Analysis API

Las bibliotecas de análisis de tinta están diseñadas para usarse en diversos entornos de programación admitidos. Hay cuatro capas básicas a través de las que la aplicación puede hacer uso del análisis de tinta. Estos niveles son:

-   Capa de Windows Forms
-   Nivel de WPF
-   El nivel COM
-   Nivel base

### <a name="windows-forms-applications"></a>Aplicaciones de Windows Forms

Puede usar la API de análisis de tinta en el proyecto administrado agregando una referencia a las siguientes bibliotecas:

-   Microsoft. Ink. Analysis (Microsoft.Ink.Analysis.dll)
-   Biblioteca de análisis de documentos de entrada manuscrita (IACore.dll)

En Windows Forms aplicaciones, lo más probable es que use las bibliotecas junto con los objetos de la plataforma de Tablet PC estándar que se encuentran en el ensamblado Microsoft Tablet PC API v 1.7. Asegúrese de que también tiene una referencia a:

-   Microsoft Tablet PC API v 1.7.2600.2180 (Microsoft.Ink.dll)

### <a name="windows-presentation-framework-applications"></a>Aplicaciones de Windows Presentation Framework

Puede usar la API de análisis de tinta en el proyecto de WPF agregando una referencia a los miembros del análisis de tinta que se definen en el espacio de nombres System. Windows. Ink en el ensamblado de IAWinFX.dll. Este ensamblado se instala mediante el SDK de.

### <a name="com-applications"></a>Aplicaciones COM

Las aplicaciones COM que no son de automatización deben usar el nivel COM de las API de análisis de tinta.

Los objetos [ContextNode](/previous-versions/ms551996(v=vs.100)) específicos de tipo, como [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100))y others, no se usan en el nivel com. En su lugar, debe usar [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) en la interfaz [**IContextNode**](icontextnode.md) estándar.

Debe \# incluir "IACom. h". Lo más probable es que use las bibliotecas junto con el objeto de tinta de la plataforma de Tablet PC, por lo que también debe \# incluir "msinkaut. h".

### <a name="rts-and-other-applications"></a>RTS y otras aplicaciones

La capa de base de análisis de tinta funciona de forma diferente a la de los demás en cuanto a los datos de punto para el análisis en lugar de los objetos de [trazo](/previous-versions/ms552692(v=vs.100)) . Algunos ejemplos de dónde trabajaría con el nivel base directamente en lugar de utilizar los niveles de Windows Forms o COM son las aplicaciones que no usan objetos de tinta de la plataforma de Tablet PC de primera generación o las aplicaciones que usan las API de [**RealTimeStylus**](realtimestylus-class.md) para administrar la entrada del lápiz en lugar de usar los objetos de [tinta](/previous-versions/ms583670(v=vs.100)) de la plataforma de Tablet PC.

## <a name="32-bit-support-only"></a>Solo compatibilidad con 32 bits

Tenga en cuenta que las bibliotecas de análisis de tinta solo se admiten en procesos de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de análisis de tinta](ink-analysis-overview.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 
