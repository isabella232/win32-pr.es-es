---
description: El esquema de impresión y las tecnologías relacionadas están disponibles en Microsoft .NET Framework 3.0 y versiones posteriores de Microsoft .NET Framework y en Windows Vista y versiones posteriores de Windows.
ms.assetid: 98d5f8ec-54bd-4e88-b632-ed427b599cb6
title: Esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3ac50b9a2f2aba9cda7dc73f183e1f3571cc9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248439"
---
# <a name="print-schema"></a>Esquema de impresión

El esquema de impresión y las tecnologías relacionadas están disponibles en Microsoft .NET Framework 3.0 y versiones posteriores de Microsoft .NET Framework y en Windows Vista y versiones posteriores de Windows. Los documentos XPS y el modelo de objetos XPS pueden usar los objetos de vale de impresión, que se describen en especificación de esquema de impresión [,](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)para especificar las preferencias de impresión de un documento en impresoras y aplicaciones de visualización.

La [especificación de esquema de](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) impresión es un documento descargable que contiene información sobre el esquema de impresión y cómo usarlo en documentos e impresión. Solo se proporciona información adicional en línea para su información, en [Referencia de esquema de impresión heredado](print-schema.md); sin embargo, es posible que no refleje con precisión la versión actual de la [especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). Consulte especificación [de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) para obtener la información de diseño más reciente.

## <a name="print-schema-overview"></a>Información general sobre el esquema de impresión

El esquema de impresión es un esquema basado en XML estructurado jerárquicamente que se usa para organizar y describir las propiedades de una impresora o un trabajo de impresión. El esquema de impresión incluye dos componentes: las palabras clave de esquema de impresión y el marco de esquema de impresión. Las palabras clave de esquema de impresión son un conjunto de instancias de elementos que describen los atributos de impresora y la intención de formato del trabajo de impresión. Print Schema Framework define una colección jerárquicamente estructurada de tipos de elementos XML y cómo estos tipos de elemento se pueden usar juntos.

Las tecnologías de esquema de impresión, denominadas *PrintCapabilities* e *PrintTicket,* se han creado con las palabras clave de esquema de impresión especificadas por el marco de esquema de impresión. La especificación de esquema de impresión admite extensiones de esquema de terceros, de modo que los usuarios del esquema de impresión no estén restringidos a las instancias property, feature, option o ParameterInit definidas por las palabras clave de esquema de impresión. Las instancias de elementos de terceros se pueden agregar a instancias de elemento definidas por las palabras clave de esquema de impresión; Sin embargo, las instancias de propiedad privadas de terceros deben pertenecer a un espacio de nombres que esté claramente asociado al tercero que creó el espacio de nombres.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Referencia de esquema de impresión heredado](print-schema.md)
</dt> <dt>

[Comunicaciones de impresora bidireccional (Centro de desarrollo de hardware)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

 

 
