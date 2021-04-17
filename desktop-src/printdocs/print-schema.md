---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Referencia de esquema de impresión heredado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881e986501950108c06e1e92303d13dc06265aae
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105660015"
---
# <a name="legacy-print-schema-reference"></a>Referencia de esquema de impresión heredado

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema de impresión y las tecnologías relacionadas están disponibles en Microsoft .NET Framework 3,0, Microsoft Windows Vista y versiones posteriores.

El esquema de impresión proporciona un formato basado en XML para expresar y organizar un conjunto grande de propiedades que describen un formato de trabajo o PrintCapabilities de manera jerárquica.

El esquema de impresión es un término genérico que incluye dos componentes, las palabras clave del esquema de impresión y el marco de trabajo del esquema de impresión. El documento imprimir palabras clave del esquema es un esquema público que define un conjunto de instancias de elementos que se pueden usar para describir los atributos de dispositivo y el formato de los trabajos de impresión. El marco de trabajo de esquema de impresión es un esquema público que define una colección jerárquicamente estructurada de tipos de elementos XML y especifica cómo se pueden usar los tipos de elementos juntos.

Las palabras clave del esquema de impresión y el marco de esquema de impresión forman la base de dos tecnologías relacionadas con el esquema de impresión, el esquema de PrintCapabilities y el esquema de PrintTicket.

Es importante tener en cuenta que uno de los objetivos del esquema de impresión es admitir las extensiones de esquema por proveedores. Es decir, los proveedores no están restringidos al uso de las instancias de propiedad, característica, opción o ParameterInit definidas en las palabras clave del esquema de impresión en las tecnologías basadas en el marco de trabajo del esquema de impresión. Las instancias de elementos específicas del proveedor pueden intercalarse libremente dentro de las instancias de elemento definidas en las palabras clave del esquema de impresión. El único requisito es que las instancias de propiedad específicas del proveedor (es decir, privadas) deben pertenecer a un espacio de nombres que esté claramente asociado al proveedor.

-   [Fondo del esquema de impresión](print-schema-background.md)

-   [Tecnologías de Schema-Related de impresión](print-schema-related-technologies.md)

-   [Términos usados en el esquema de impresión](terms-used-in-the-print-schema.md)

-   [Sintaxis del esquema de impresión](syntax-of-the-print-schema.md)

-   [Resumen de tipos de elemento](summary-of-element-types.md)

-   [Marco de esquema de impresión](print-schema-framework.md)

-   [Palabras clave públicas de esquema de impresión](print-schema-public-keywords.md)

-   [Esquema y construcción de documentos de PrintCapabilities](printcapabilities-schema-and-document-construction.md)

-   [Esquema PrintTicket y construcción de documentos](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



