---
description: Los proveedores de PrintCapabilities deben admitir un conjunto mínimo de funcionalidades, que están implícitas en la interfaz del proveedor PrintTicket/PrintCapabilities.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilidades de los proveedores de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc04137eacdd2395205b96233db3c53964bc02
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404918"
---
# <a name="responsibilities-of-printcapabilities-providers"></a>Responsabilidades de los proveedores de PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Los proveedores de PrintCapabilities deben admitir un conjunto mínimo de funcionalidades, que están implícitas en la interfaz del proveedor PrintTicket/PrintCapabilities. Esta funcionalidad se incluye a continuación.

-   ¿Deben seguir la dirección de la propagación?? Atributo XML, cuando aparece en el contexto adecuado y contiene un valor válido para ese contexto.

-   Deben generar un documento PrintCapabilities que se ajuste al esquema PrintCapabilities y cumpla los requisitos especificados en el esquema de impresión.

-   Deben poder reconocer un PrintTicket válido.

-   Deben poder interpretar un PrintTicket y comprender la configuración específica que representa.

-   Deben ser capaces de determinar si esa configuración contiene conflictos de restricción.

-   Deben poder modificar un PrintTicket no válido o en conflicto realizando el cambio menos significativo necesario para que sea válido y sin conflictos.

-   Deben poder generar un documento PrintCapabilities para una configuración de dispositivo determinada.

-   Deben poder generar una configuración predeterminada o PrintTicket.

-   Deben poder generar un documento PrintCapabilities que se corresponda con la configuración predeterminada.

-   Deben implementar un proceso de puntuación de opciones definido por el controlador de dispositivo capaz de determinar la proximidad de la coincidencia entre dos instancias de opción que pertenecen a la misma característica. Este algoritmo se usa en el proceso de validación PrintTicket.

Además de los requisitos anteriores, el documento PrintCapabilities debe contener valores válidos y correctos para cada atributo XML (por ejemplo, restringido) de cada opción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



