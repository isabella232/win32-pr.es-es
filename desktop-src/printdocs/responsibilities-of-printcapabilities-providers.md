---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilidades de los proveedores de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bbf355f7b62f8f9c8b3f3b0c59714cdd6ade5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698002"
---
# <a name="responsibilities-of-printcapabilities-providers"></a>Responsabilidades de los proveedores de PrintCapabilities

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Los proveedores de PrintCapabilities deben admitir un conjunto mínimo de funciones, que son implícitas por la interfaz del proveedor de PrintTicket/PrintCapabilities. Estas funcionalidades se enumeran aquí.

-   Deben seguir la dirección de la propagación? Atributo XML, cuando aparece en el contexto adecuado y contiene un valor válido para ese contexto.

-   Deben generar un documento de PrintCapabilities que se ajuste al esquema de PrintCapabilities y satisfaga los requisitos especificados en el esquema de impresión.

-   Deben ser capaces de reconocer un PrintTicket válido.

-   Deben ser capaces de interpretar un PrintTicket y comprender la configuración específica que representa.

-   Deben ser capaces de determinar si la configuración contiene conflictos de restricción.

-   Deben poder modificar un PrintTicket no válido o en conflicto mediante la realización del cambio menos significativo necesario para que sea válido y sin conflictos.

-   Deben poder generar un documento de PrintCapabilities para una configuración de dispositivo concreta.

-   Deben poder generar una configuración o un PrintTicket predeterminados.

-   Deben poder generar un documento de PrintCapabilities que se corresponda con la configuración predeterminada.

-   Deben implementar un proceso de puntuación de opciones definido por el controlador de dispositivo capaz de determinar la proximidad de la coincidencia entre dos instancias de opción que pertenecen a la misma característica. Este algoritmo se usa en el proceso de validación de PrintTicket.

Además de los requisitos anteriores, el documento de PrintCapabilities debe contener valores válidos y correctos para cada atributo XML (por ejemplo, restringido) de cada opción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



