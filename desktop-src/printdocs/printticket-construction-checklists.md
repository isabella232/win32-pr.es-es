---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Listas de comprobación de construcción de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e742bcd3b94c5016fda6f97e2fb5e20a2cf70f73
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105697986"
---
# <a name="printticket-construction-checklists"></a>Listas de comprobación de construcción de PrintTicket

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En esta sección se muestra cómo el autor de un cliente PrintTicket puede usar los tipos de elemento definidos en el marco de trabajo del esquema de impresión para crear un PrintTicket que describa los intentos de un dispositivo. El PrintTicket puede ser genérico (no vinculado a un dispositivo específico) o puede ser específico del dispositivo. La semántica del PrintTicket se presenta con mayor detalle. Además, esta sección contiene información general sobre los conceptos y la terminología que se describen con más detalle en secciones posteriores.

Hay dos enfoques fundamentalmente diferentes para construir un PrintTicket. Se puede usar cualquiera de estos enfoques.

-   Destine el PrintTicket a un dispositivo genérico o desconocido mediante la [creación de un PrintTicket genérico](creating-a-generic-printticket.md).

    Si el objetivo principal es conservar la intención del usuario final, es posible que quiera tomar este enfoque mediante la construcción y el almacenamiento de un PrintTicket genérico no validado con el documento.

-   Establecer como destino el PrintTicket en un dispositivo específico mediante la [creación de un Device-Specific PrintTicket](creating-a-device-specific-printticket.md).

    Si está más interesado en sacar provecho de todas las características que ofrece un dispositivo determinado, puede tomar este enfoque mediante la construcción de un PrintTicket para el dispositivo específico y el almacenamiento del PrintTicket validado con el documento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



