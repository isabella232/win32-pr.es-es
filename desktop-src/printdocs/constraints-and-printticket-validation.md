---
description: Para evitar conflictos de restricciones, los proveedores de PrintTicket deben admitir la validación que los clientes usan para realizar la validación en su PrintTicket.
ms.assetid: f4c66812-8782-4a85-8a74-3505c4e73e56
title: Restricciones y validación de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08abc07f0ef96e94720f8f9431a192e5dbcac669
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409578"
---
# <a name="constraints-and-printticket-validation"></a>Restricciones y validación de PrintTicket

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Como se describe en la sección Esquema de PrintCapabilities, algunos de los posibles resultados de configuración expresados en un documento PrintCapabilities no son válidos para el dispositivo. Se dice que las configuraciones que no son válidas contienen conflictos de restricciones (un término que se usa en el mundo de los archivos PPD/GPD). Para evitar conflictos de restricciones, los proveedores de PrintTicket deben admitir una operación de validación PrintTicket que los clientes usan para realizar la validación en su PrintTicket. Esta operación debe detectar si la configuración especificada puede producirse en el dispositivo. Si no se puede producir la configuración (porque los elementos Feature y Option especificados no existen en el dispositivo actual o porque la configuración está restringida), la operación debe modificar la entrada PrintTicket para que contenga valores válidos sin restricciones. La operación también puede quitar o validar otra información en PrintTicket. Tenga en cuenta que cuando se encuentra un conflicto de restricción, el código de validación debe cambiar la configuración de uno de los atributos de dispositivo para evitar el conflicto de restricción. [Las definiciones de opciones](option-definitions.md) sugieren que se debe usar un proceso de puntuación definido por el controlador de dispositivo para determinar qué atributo de dispositivo se debe cambiar para conservar mejor la intención original del usuario. El código de validación podría codificar de forma hardcode el proceso de puntuación para favorecer un atributo de dispositivo sobre otro, o bien podría usar la información proporcionada por una instancia de propiedad determinada en PrintTicket para guiar la resolución. Dado que no hay ninguna propiedad definida en las palabras clave de esquema de impresión que permita a los clientes especificar la prioridad relativa de cada atributo de dispositivo, es probable que otros proveedores de PrintTicket ignoren los elementos de propiedad PrintTicket privados utilizados para este propósito.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



