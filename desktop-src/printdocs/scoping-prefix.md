---
description: Un prefijo de ámbito es una etiqueta textual anexada previamente a una palabra clave de esquema para proporcionar un ámbito contextual, incluidos Trabajo, Documento y Página.
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: Prefijo de ámbito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c027de94fda403eb58905e536d8c6256cb2d6c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404908"
---
# <a name="scoping-prefix"></a>Prefijo de ámbito

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un prefijo de ámbito es una etiqueta textual anexada previamente a una palabra clave de esquema para proporcionar un ámbito contextual. Esto permite la suscripción de un contexto específico y bien comprendido a las palabras clave de una manera predefinida. La característica de esquema de impresión, ParameterDef, ParameterInit y ParameterRef y la palabra clave Property de nivel raíz Elements DEBEN tener uno de los prefijos de ámbito siguientes: "Job", "Document" o "Page".

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a>Interpretación del prefijo de ámbito con contenido PrintTicket

PrintTicket se puede dividir en tres niveles de contenido que representan el trabajo de alto nivel, los documentos del trabajo y las páginas de cada documento. Estos niveles se clasifican según la especificidad; El nivel de trabajo es más general, a continuación, el nivel de documento y, a continuación, el nivel de página es más específico. Un trabajo consta de uno o varios documentos y un documento consta de una o varias páginas.

## <a name="job-level-prefix"></a>Prefijo de nivel de trabajo

Un vale de nivel de trabajo contiene toda la configuración de formato de trabajo diseñada para aplicarse a un trabajo completo. Los elementos con prefijos de ámbito "Job", "Document" o "Page" se permiten en un vale de nivel de trabajo.

La configuración con prefijo "Documento" y "Página" especificada en un vale de nivel de trabajo se aplicará automáticamente a los vales de nivel de página y documento.

## <a name="document-level-prefix"></a>Prefijo de nivel de documento

El vale de nivel de documento incorpora cualquier configuración de formato de trabajo diseñada para aplicarse a uno o varios documentos de un trabajo. Esto puede incluir la configuración especificada previamente en el vale de nivel de trabajo. Solo se permiten elementos con prefijos de ámbito de "Documento" o "Página" en un vale de nivel de documento.

Un vale de nivel de documento puede contener la configuración con prefijo de documento especificada previamente por el vale de nivel de trabajo.

## <a name="page-level-prefix"></a>Prefijo de nivel de página

El vale de nivel de página incorpora cualquier configuración de formato de trabajo destinada a aplicar a una o varias páginas un trabajo (no limitado a un único documento). Esto puede incluir la configuración especificada previamente en el vale Trabajo o Nivel de documento. Solo se permiten elementos con prefijos de ámbito de "Página" en un vale de nivel de página.

Un vale de nivel de página puede contener la configuración con prefijo "Página" especificada previamente por el vale de nivel de trabajo o el vale de nivel de documento.

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a>Prefijo de uso dentro de un documento de capacidades de impresión o PrintTicket

Los documentos PrintTicket e PrintCapabilities NO DEBEN contener varias palabras clave que solo difieren en el prefijo de ámbito. Por ejemplo, un documento PrintCapabilities NO DEBE tener especificados JobInputBin y PageInputBin. Sin embargo, un documento de capacidades de impresión PUEDE tener tanto JobDuplexAllDocumentsContiguously como DocumentDuplex especificados porque se consideran características diferentes, ya que presentan un comportamiento diferente. Este ejemplo también es true para un único PrintTicket.

## <a name="prefix-conflict-management"></a>Administración de conflictos de prefijos

Un conflicto de palabras clave entre la configuración se define como, el mismo elemento de esquema de impresión de nivel raíz que indica el atributo XML "name", que aparece en varios vales de nivel. Si no hay ningún conflicto, un elemento con ámbito de prefijo se puede insertar o heredar de un vale más general a un vale más específico. Si hay un conflicto, la configuración del vale más específico tiene prioridad. Es decir, la configuración por página de un vale de nivel de página invalida la configuración idéntica por página en un vale de nivel de trabajo o documento. De forma similar, la configuración del documento en el vale de nivel de documento tiene prioridad sobre la configuración del documento en el vale de nivel de trabajo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



