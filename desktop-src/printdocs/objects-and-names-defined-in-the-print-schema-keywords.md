---
description: El marco de trabajo de esquema de impresión define un espacio de nombres que incluye los elementos y atributos XML definidos en las palabras clave de esquema de impresión.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Objetos y nombres definidos en las palabras clave de esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aabdac90de6743388ca1f4d44e1ad52c020dbd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408558"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a>Objetos y nombres definidos en las palabras clave de esquema de impresión

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El marco de trabajo de esquema de impresión define un espacio de nombres que incluye los elementos y atributos XML definidos en las palabras clave de esquema de impresión. Esto incluye elementos como Feature, Option y ScoredProperty; nombres de atributo como name y propagate; y valores para atributos XML, como restringidos. En otras palabras, cada uso de un nombre definido en las palabras clave de esquema de impresión debe calificarse explícitamente con este espacio de nombres o debe asociarse implícitamente a este espacio de nombres mediante el uso de un atributo xmlns predeterminado. El documento Palabras clave de esquema de impresión define las instancias de elementos públicos que pueden aparecer en cualquier contexto o ubicación determinados. Las instancias de elemento solo deben aparecer dentro del contexto o la ubicación designados en el marco de esquema de impresión. Por ejemplo, la instancia de <psf:Option name= "psk:Letter"> definida en las palabras clave de esquema de impresión debe aparecer dentro de la instancia de <psf:Feature name = "psk:PageMediaSize"> (también se define en las palabras clave de esquema de impresión). No tiene la libertad de usar una instancia de Option determinada fuera de su contexto especificado.

Las instancias de elementos definidas de forma privada pueden aparecer en cualquier lugar, siempre que el tipo de elemento aparezca en un contexto permitido por el marco de esquema de impresión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



