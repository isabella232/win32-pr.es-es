---
description: 'Hay cuatro capas en la biblioteca ink Analysis: Windows Forms, WPF, COM y la capa base. En esta sección se describe cuándo usar cada capa.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Uso de Ink Analysis API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdfada58868c7fe959f832e0c1243bc91a373fb0186d8deee2f9481d78a95714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032353"
---
# <a name="ink-analysis-api-usage"></a>Uso de Ink Analysis API

Hay cuatro capas en la biblioteca ink Analysis: Windows Forms, WPF, COM y la capa base. En esta sección se describe cuándo usar cada capa.

## <a name="ink-analysis-api-overview"></a>Información general de Ink Analysis API

Las bibliotecas de análisis de lápiz están diseñadas para usarse en una variedad de entornos de programación compatibles. Hay cuatro capas básicas a través de las cuales la aplicación puede hacer uso del análisis de entrada de lápiz. Estas capas son:

-   La capa Windows Forms
-   La capa de WPF
-   La capa COM
-   La capa base

### <a name="windows-forms-applications"></a>Aplicaciones de Windows Forms

Puede usar Ink Analysis API en el proyecto administrado agregando una referencia a las bibliotecas siguientes:

-   Microsoft.Ink.Analysis (Microsoft.Ink.Analysis.dll)
-   Biblioteca de análisis de documentos de Ink (IACore.dll)

En Windows Forms, lo más probable es que use las bibliotecas junto con los objetos de plataforma estándar de Tablet PC que se encuentran en el ensamblado microsoft Tablet PC API v1.7. Asegúrese de que también tiene una referencia a:

-   Microsoft Tablet PC API v1.7.2600.2180 (Microsoft.Ink.dll)

### <a name="windows-presentation-framework-applications"></a>Windows Aplicaciones de Presentation Framework

Puede usar Ink Analysis API en el proyecto de WPF agregando una referencia a los miembros de Análisis de entrada de lápiz definidos en el sistema. Windows. Espacio de nombres ink en el IAWinFX.dll ensamblado. El SDK instala este ensamblado.

### <a name="com-applications"></a>Aplicaciones COM

Las aplicaciones COM que no son de Automatización deben usar la capa COM de las API de análisis de lápiz.

Los objetos [ContextNode específicos](/previous-versions/ms551996(v=vs.100)) del tipo (como [ParagraphNode,](/previous-versions/ms580136(v=vs.100)) [InkWordNode](/previous-versions/ms580133(v=vs.100))y otros) no se usan en la capa COM. En su lugar, debe usar [**IContextNode::AddPropertyData en**](icontextnode-addpropertydata.md) la interfaz [**IContextNode**](icontextnode.md) estándar.

Debe incluir \# "IACom.h". Lo más probable es que use las bibliotecas junto con el objeto Ink de la plataforma de Tablet PC, por lo que también debe incluir \# "msyecciónut.h".

### <a name="rts-and-other-applications"></a>RTS y otras aplicaciones

La capa base Análisis de entrada de lápiz funciona de forma diferente a las demás, ya que toma datos de punto para el análisis en lugar de [objetos Stroke.](/previous-versions/ms552692(v=vs.100)) Entre los ejemplos de dónde trabajaría con la capa base directamente en lugar de usar los formularios Windows o las capas COM, se incluyen aplicaciones que no usan objetos [](/previous-versions/ms583670(v=vs.100)) de entrada de lápiz de la plataforma pc de tableta de primera generación, o aplicaciones que usan las API [**de RealTimeStylus**](realtimestylus-class.md) para administrar la entrada de lápiz en lugar de usar los objetos de lápiz de la plataforma de Tablet PC.

## <a name="32-bit-support-only"></a>Solo compatibilidad de 32 bits

Tenga en cuenta que las bibliotecas de análisis de entrada de lápiz solo se admiten en procesos de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre análisis de entrada de lápiz](ink-analysis-overview.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 
