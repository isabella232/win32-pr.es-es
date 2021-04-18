---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Crear un documento de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccb1adf4626254ba9f71c706ad7d4556a23aeb6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707581"
---
# <a name="creating-a-printcapabilities-document"></a>Crear un documento de PrintCapabilities

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Una vez validada una PrintTicket, se puede usar para crear una instantánea de la PrintCapabilities. El proveedor debe tener una representación interna para cualquier propiedad cuyo valor dependa de la configuración del dispositivo. Por ejemplo, si SpotDiameter es una propiedad que depende de las características Resolution y MediaType, puede aparecer una representación interna de SpotDiameter en relación con los distintos valores para la resolución y el valor de MediaType, tal como se muestra en la tabla siguiente:



| Solución      | MediaType         | SpotDiameter   |
|-----------------|-------------------|----------------|
| 300<br/>  | Obligación<br/>   | 520<br/> |
| 300<br/>  | Fotográfico<br/> | 350<br/> |
| 600<br/>  | Obligación<br/>   | 330<br/> |
| 600<br/>  | Fotográfico<br/> | 180<br/> |
| 1200<br/> | Obligación<br/>   | 250<br/> |
| 1200<br/> | Fotográfico<br/> | 100<br/> |



 

En este ejemplo, el proveedor de PrintCapabilities debe usar el elemento PrintTicket proporcionado para seleccionar la entrada adecuada de la tabla interna e informar como el valor de la propiedad SpotDiameter. Este proceso se repite para cada propiedad de varios valores (para cada propiedad cuyo valor depende de la configuración). En la sección [esquema de PrintCapabilities y construcción de documentos](printcapabilities-schema-and-document-construction.md) se describen los demás pasos implicados en la creación de una instantánea de PrintCapabilities.

Para crear una instantánea del documento de PrintCapabilities predeterminado, proporcione un PrintTicket predeterminado (en lugar de un PrintTicket arbitrario) al método que crea los documentos de PrintCapabilities.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




