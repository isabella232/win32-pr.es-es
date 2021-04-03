---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: Prefijo de ámbito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef74be192671124872e19e87973a266da4a09226
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914242"
---
# <a name="scoping-prefix"></a>Prefijo de ámbito

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un prefijo de ámbito es una etiqueta de texto previamente anexada a una palabra clave de esquema para proporcionar un ámbito contextual. Esto permite la sucripción de un contexto específico y bien entendido a las palabras clave de una manera predefinida. La característica de esquema de impresión, ParameterDef, ParameterInit y ParameterRef y los elementos de palabra clave de propiedad de nivel de raíz deben tener uno de los siguientes prefijos de ámbito: "Job", "Document" o "Page".

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a>Interpretación del prefijo de ámbito con el contenido de PrintTicket

El PrintTicket puede dividirse en tres niveles de contenido que representan el trabajo de alto nivel, los documentos del trabajo y las páginas de cada documento. Estos niveles se clasifican según la especificidad; el nivel de trabajo es más general, el nivel de documento y, a continuación, el nivel de página es más específico. Un trabajo consta de uno o varios documentos y un documento consta de una o varias páginas.

## <a name="job-level-prefix"></a>Prefijo de nivel de trabajo

Un vale de nivel de trabajo contiene toda la configuración de formato del trabajo que se va a aplicar a todo un trabajo. Los elementos con prefijos de ámbito "Job", "Document" o "Page" se permiten en un vale de nivel de trabajo.

Los valores prefijos de "documento" y "página" especificados en un vale de nivel de trabajo se aplicarán automáticamente a los vales de nivel de documento y de página.

## <a name="document-level-prefix"></a>Prefijo de nivel de documento

El vale de nivel de documento incorpora cualquier configuración de formato de trabajo diseñada para aplicarse a uno o varios documentos de un trabajo. Estos pueden incluir los valores especificados previamente en el vale de nivel de trabajo. Solo se permiten elementos con prefijos de ámbito de "Document" o "Page" en un vale de nivel de documento.

Un vale de nivel de documento puede contener valores prefijos de documento especificados previamente por el vale de nivel de trabajo.

## <a name="page-level-prefix"></a>Prefijo de nivel de página

El vale de nivel de página incorpora cualquier configuración de formato de trabajo diseñada para aplicarse a una o varias páginas de un trabajo (no limitado a un único documento). Estos pueden incluir los valores especificados previamente en el vale de nivel de documento o de trabajo. Solo se permiten elementos con prefijos de ámbito de "Page" en un vale de nivel de página.

Un vale de nivel de página puede contener la configuración de prefijo "página" especificada previamente por el vale de nivel de trabajo o el vale de nivel de documento.

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a>Uso de prefijos dentro de un documento de capacidades de impresión o PrintTicket

Los documentos PrintTicket y PrintCapabilities no deben contener varias palabras clave que solo difieran en el prefijo de ámbito. Por ejemplo, un documento de PrintCapabilities no debe tener JobInputBin y PageInputBin especificados.? Sin embargo, un documento de funcionalidades de impresión puede tener JobDuplexAllDocumentsContiguously y DocumentDuplex especificados porque se consideran características diferentes, ya que presentan un comportamiento diferente. Este ejemplo también se cumple para un único PrintTicket.

## <a name="prefix-conflict-management"></a>Administración de conflictos de prefijo

Un conflicto de palabras clave entre valores se define como, el mismo elemento de esquema de impresión de nivel raíz indicado por el atributo XML "Name", que aparece en varios vales de nivel. Si no hay ningún conflicto, un elemento con ámbito de prefijo se puede insertar o heredar de un vale más general en un vale más específico. Si hay un conflicto, la configuración del vale más específico tiene prioridad. Es decir, la configuración de cada página en un vale de nivel de página invalida la configuración de cada página idéntica en un documento o un vale de nivel de trabajo. Del mismo modo, la configuración de documento en el vale de nivel de documento tiene prioridad sobre la configuración de documento en el vale de nivel de trabajo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



