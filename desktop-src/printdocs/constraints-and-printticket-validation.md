---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: Restricciones y validación de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddcc1f6f3ad496b6bfb6ed201cf93c2b4a10679
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104003458"
---
# <a name="constraints-and-printticket-validation"></a>Restricciones y validación de PrintTicket

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Como se describe en la sección esquema de PrintCapabilities, algunos de los resultados de configuración posibles que se expresan en un documento de PrintCapabilities no son válidos para el dispositivo. Se dice que las configuraciones no válidas contienen conflictos de restricción (un término usado en el mundo de archivos PPD/GPD). Para evitar conflictos de restricción, los proveedores de PrintTicket deben admitir una operación de validación de PrintTicket que los clientes usan para realizar la validación en su PrintTicket. Esta operación debe detectar si la configuración especificada puede producirse en el dispositivo. Si no se puede realizar la configuración (porque los elementos de característica y opción especificados no existen en el dispositivo actual, o porque la configuración está restringida), la operación debe modificar el PrintTicket de entrada para que contenga una configuración válida y sin restricciones. La operación podría quitar o validar también otra información en el PrintTicket. Tenga en cuenta que cuando se encuentra un conflicto de restricción, el código de validación debe cambiar la configuración de uno de los atributos del dispositivo para evitar el conflicto de restricción. Las [definiciones de opciones](option-definitions.md) sugieren que se debe usar un proceso de puntuación definido por un controlador de dispositivo para determinar qué atributo de dispositivo debe cambiarse con el fin de preservar mejor la intención original del usuario. El código de validación podría codificar el proceso de puntuación para favorecer un atributo de dispositivo sobre otro, o podría usar la información proporcionada por una instancia de propiedad determinada en el PrintTicket para guiar la resolución. Dado que no hay ninguna propiedad definida en las palabras clave del esquema de impresión que permita a los clientes especificar la prioridad relativa de cada atributo de dispositivo, es probable que otros proveedores de PrintTicket omitan los elementos de propiedad PrintTicket privados usados para este propósito.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



