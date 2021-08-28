---
description: Vea cómo el autor de un cliente PrintTicket puede usar tipos de elemento para crear un PrintTicket que describe las intenciones de un dispositivo.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Listas de comprobación de construcción de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6a3ae0c19fea01738dbf7c6ecfa52f6f156d59f67dae89d6d5a2952059a765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091725"
---
# <a name="printticket-construction-checklists"></a>Listas de comprobación de construcción de PrintTicket

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En esta sección se muestra cómo el autor de un cliente PrintTicket puede usar los tipos de elemento definidos en el marco de esquema de impresión para crear un PrintTicket que describa las intenciones de un dispositivo. PrintTicket puede ser genérico (no vinculado a un dispositivo específico) o puede ser específico del dispositivo. La semántica de PrintTicket se presenta con más detalle. Además, esta sección contiene información general sobre conceptos y terminología que se tratan con más detalle en secciones posteriores.

Hay dos enfoques fundamentalmente diferentes para construir un PrintTicket. Se puede usar cualquier enfoque.

-   Para dirigir PrintTicket a un dispositivo desconocido o genérico, [cree un printticket genérico.](creating-a-generic-printticket.md)

    Si el objetivo principal es conservar la intención del usuario final, es posible que desee seguir este enfoque mediante la construcción y el almacenamiento de un PrintTicket genérico no validado con el documento.

-   Para dirigir PrintTicket a un dispositivo específico, cree [un Device-Specific PrintTicket](creating-a-device-specific-printticket.md).

    Si está más interesado en aprovechar todas las características que ofrece un dispositivo determinado, puede que desee seguir este enfoque mediante la construcción de un PrintTicket para el dispositivo específico y el almacenamiento del PrintTicket validado con el documento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



