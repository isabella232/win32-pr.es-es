---
description: Vea cómo el autor de un cliente PrintTicket puede usar tipos de elemento para crear un PrintTicket que describa las intenciones de un dispositivo.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Listas de comprobación de construcción de PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76d47911d0060cc6d06604bfaeaa4abcebd3daa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359702"
---
# <a name="printticket-construction-checklists"></a>Listas de comprobación de construcción de PrintTicket

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En esta sección se muestra cómo el autor de un cliente PrintTicket puede usar los tipos de elementos definidos en el marco de esquema de impresión para crear un PrintTicket que describa las intenciones de un dispositivo. PrintTicket puede ser genérico (no vinculado a un dispositivo específico) o puede ser específico del dispositivo. La semántica de PrintTicket se presenta con más detalle. Además, esta sección contiene información general de conceptos y terminología que se tratan con más detalle en secciones posteriores.

Hay dos enfoques fundamentalmente diferentes para construir un PrintTicket. Se puede usar cualquier enfoque.

-   Para dirigir PrintTicket a un dispositivo desconocido o genérico, [cree un PrintTicket genérico.](creating-a-generic-printticket.md)

    Si el objetivo principal es conservar la intención del usuario final, es posible que quiera seguir este enfoque mediante la construcción y el almacenamiento de un printTicket genérico no validado con el documento.

-   Para dirigir PrintTicket a un dispositivo específico, cree [un Device-Specific PrintTicket](creating-a-device-specific-printticket.md).

    Si está más interesado en aprovechar todas las características que ofrece un dispositivo determinado, es posible que quiera seguir este enfoque mediante la construcción de un PrintTicket para el dispositivo específico y el almacenamiento del PrintTicket validado con el documento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



