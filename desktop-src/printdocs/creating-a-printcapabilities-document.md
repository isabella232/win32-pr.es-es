---
description: Después de validar printticket, se puede usar para crear una instantánea de PrintCapabilities.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Crear un documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1a01395df674b683349bd4a5f42fe1bd57ef2768ef4d967ba3aeda7734f5e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950205"
---
# <a name="creating-a-printcapabilities-document"></a>Crear un documento PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Después de validar printticket, se puede usar para crear una instantánea de PrintCapabilities. El proveedor debe tener una representación interna para cualquier propiedad cuyo valor depende de la configuración del dispositivo. Por ejemplo, si SpotDiameter es una propiedad que depende de las características Resolution y MediaType, una representación interna de SpotDiameter en relación con los distintos valores de Resolution y MediaType podría aparecer como en la tabla siguiente:



| Resolución      | MediaType         | SpotDiameter   |
|-----------------|-------------------|----------------|
| 300<br/>  | vinculación<br/>   | 520<br/> |
| 300<br/>  | Brillante<br/> | 350<br/> |
| 600<br/>  | vinculación<br/>   | 330<br/> |
| 600<br/>  | Brillante<br/> | 180<br/> |
| 1200<br/> | vinculación<br/>   | 250<br/> |
| 1200<br/> | Brillante<br/> | 100<br/> |



 

En este ejemplo, el proveedor PrintCapabilities debe usar el PrintTicket proporcionado para seleccionar la entrada adecuada de la tabla interna y notificarlo como valor de la propiedad SpotDiameter. Este proceso se repite para cada propiedad multivalor (para cada propiedad cuyo valor depende de la configuración). En [la sección Esquema de PrintCapabilities](printcapabilities-schema-and-document-construction.md) y Construcción de documentos se describen los demás pasos necesarios para crear una instantánea de PrintCapabilities.

Para crear una instantánea del documento PrintCapabilities predeterminado, proporcione un PrintTicket predeterminado (en lugar de un PrintTicket arbitrario) al método que crea documentos PrintCapabilities.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




