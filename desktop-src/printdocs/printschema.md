---
description: El esquema de impresión y las tecnologías relacionadas están disponibles en Microsoft .NET Framework 3,0 y versiones posteriores de Microsoft .NET Framework y en Windows Vista y versiones posteriores de Windows.
ms.assetid: 98d5f8ec-54bd-4e88-b632-ed427b599cb6
title: Imprimir esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3ac50b9a2f2aba9cda7dc73f183e1f3571cc9d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689688"
---
# <a name="print-schema"></a>Imprimir esquema

El esquema de impresión y las tecnologías relacionadas están disponibles en Microsoft .NET Framework 3,0 y versiones posteriores de Microsoft .NET Framework y en Windows Vista y versiones posteriores de Windows. Los documentos XPS y el modelo de objetos de XPS pueden utilizar los objetos de vale de impresión, que se describen en la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip), para especificar las preferencias de impresión de un documento en impresoras y ver aplicaciones.

La [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) es un documento descargable que contiene información sobre el esquema de impresión y cómo se usa en los documentos y la impresión. Solo se proporciona información adicional en línea para su información, en [referencia de esquema de impresión heredada](print-schema.md). sin embargo, es posible que no refleje con precisión la versión actual de la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). Consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) para obtener la información de diseño más actual.

## <a name="print-schema-overview"></a>Información general sobre el esquema de impresión

El esquema de impresión es un esquema basado en XML estructurado jerárquicamente que se utiliza para organizar y describir las propiedades de una impresora o un trabajo de impresión. El esquema de impresión incluye dos componentes: las palabras clave del esquema de impresión y el marco de trabajo del esquema de impresión. Las palabras clave del esquema de impresión son un conjunto de instancias de elementos que describen los atributos de la impresora y el intento de formato del trabajo de impresión. El marco de trabajo del esquema de impresión define una colección jerárquicamente estructurada de tipos de elementos XML y cómo estos tipos de elementos se pueden usar juntos.

Las tecnologías de esquema de impresión, denominadas *PrintCapabilities* y *PrintTicket*, se crean con las palabras clave del esquema de impresión tal y como se especifica en el marco de trabajo del esquema de impresión. La especificación del esquema de impresión admite extensiones de esquema por parte de terceros, de modo que los usuarios del esquema de impresión no se limiten a las instancias de propiedad, característica, opción o ParameterInit definidas por las palabras clave del esquema de impresión. Las instancias de elemento de terceros se pueden agregar a instancias de elemento definidas por las palabras clave del esquema de impresión; sin embargo, las instancias de propiedad de terceros privadas deben pertenecer a un espacio de nombres que esté claramente asociado al tercero que creó el espacio de nombres.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Referencia de esquema de impresión heredado](print-schema.md)
</dt> <dt>

[Comunicaciones de impresora bidireccional (centro de desarrollo de hardware)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

 

 
