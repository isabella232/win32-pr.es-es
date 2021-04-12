---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Objetos y nombres definidos en las palabras clave del esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2347c73dd647f90a88821658cdcf9e2ed846e83
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279859"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a>Objetos y nombres definidos en las palabras clave del esquema de impresión

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El marco de trabajo del esquema de impresión define un espacio de nombres que incluye los elementos y los atributos XML definidos en las palabras clave del esquema de impresión. Esto incluye elementos como Feature, Option y ScoredProperty; nombres de atributo como Name y Propagate; los valores y para los atributos XML, como Constrained. En otras palabras, cada uso de un nombre que se define en las palabras clave del esquema de impresión se debe calificar explícitamente con este espacio de nombres o se debe asociar implícitamente a este espacio de nombres mediante el uso de un atributo xmlns predeterminado. El documento imprimir palabras clave del esquema define las instancias del elemento público que pueden aparecer en cualquier contexto o ubicación determinados. Las instancias de elemento deben aparecer solo en el contexto o la ubicación designada en el marco de trabajo del esquema de impresión. Por ejemplo, la <PSF: Option name = "PSK: Letter" > instancia que se define en las palabras clave del esquema de impresión debe aparecer dentro de la <PSF: Feature name = "PSK: PageMediaSize" > (también se define en las palabras clave del esquema de impresión). No tiene la libertad de usar una instancia de opción determinada fuera de su contexto especificado.

Las instancias de elementos definidas de forma privada pueden aparecer en cualquier parte siempre que el tipo de elemento aparezca en un contexto permitido por el marco de trabajo del esquema de impresión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



