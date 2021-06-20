---
description: En esta introducción se describen los temas de referencia Esquema de impresión y vínculos a Esquema de impresión. El esquema de impresión incluye las palabras clave de esquema de impresión y el marco de trabajo.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Referencia de esquema de impresión heredado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a8f417d20913563cfd4a52ba51d21b516e73f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407138"
---
# <a name="legacy-print-schema-reference"></a>Referencia de esquema de impresión heredado

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema de impresión y las tecnologías relacionadas están disponibles en Microsoft .NET Framework 3.0, Microsoft Windows Vista y versiones posteriores.

El esquema de impresión proporciona un formato basado en XML para expresar y organizar un gran conjunto de propiedades que describen un formato de trabajo o PrintCapabilities de una manera jerárquicamente estructurada.

El esquema de impresión es un término paraguas que incluye dos componentes, las palabras clave de esquema de impresión y el marco de esquema de impresión. El documento Palabras clave de esquema de impresión es un esquema público que define un conjunto de instancias de elemento que se pueden usar para describir los atributos del dispositivo y el formato del trabajo de impresión. Print Schema Framework es un esquema público que define una colección jerárquicamente estructurada de tipos de elementos XML y especifica cómo se pueden usar conjuntamente los tipos de elemento.

Las palabras clave de esquema de impresión y el marco de esquema de impresión forman la base de dos tecnologías relacionadas con el esquema de impresión, el esquema PrintCapabilities y el esquema PrintTicket.

Es importante tener en cuenta que uno de los objetivos del esquema de impresión es admitir las extensiones de esquema por parte de los proveedores. Es decir, los proveedores no están restringidos a usar solo las instancias property, feature, option o ParameterInit definidas en las palabras clave de esquema de impresión en las tecnologías creadas en el marco de esquema de impresión. Las instancias de elementos específicas del proveedor se pueden intercalar libremente dentro de las instancias de elemento definidas en las palabras clave de esquema de impresión. El único requisito es que las instancias de propiedad específicas del proveedor (es decir, privadas) deben pertenecer a un espacio de nombres que esté claramente asociado al proveedor.

-   [Fondo del esquema de impresión](print-schema-background.md)

-   [Tecnologías de Schema-Related impresión](print-schema-related-technologies.md)

-   [Términos usados en el esquema de impresión](terms-used-in-the-print-schema.md)

-   [Sintaxis del esquema de impresión](syntax-of-the-print-schema.md)

-   [Resumen de los tipos de elemento](summary-of-element-types.md)

-   [Marco de esquema de impresión](print-schema-framework.md)

-   [Palabras clave públicas del esquema de impresión](print-schema-public-keywords.md)

-   [Esquema PrintCapabilities y construcción de documentos](printcapabilities-schema-and-document-construction.md)

-   [Esquema PrintTicket y construcción de documentos](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



