---
title: Esquema de eventos
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: 'Más información sobre: Esquema de eventos'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bfb26f6c71d544e0c0a6a4d833b40a5d15ae5485
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361745"
---
# <a name="event-schema"></a>Esquema de eventos

El esquema event define los siguientes elementos y tipos que identifican los elementos y atributos de un evento registrado:

-   [Elementos EventSchema](eventschema-elements.md)
-   [Tipos simples de EventSchema](eventschema-simple-types.md)
-   [Tipos complejos de EventSchema](eventschema-complex-types.md)

La sección elements contiene los nombres de los elementos que encontraría en un evento registrado; sin embargo, para obtener los detalles de cada elemento, vea el tipo complejo que contiene el elemento.

El SDK Windows incluye el esquema en el \\ archivo \\ Include Event.xsd.

Puede usar este esquema para identificar los elementos y atributos al llamar a la función [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) para representar secciones o propiedades específicas del evento. Para obtener un ejemplo en el que se muestra cómo usar este esquema al representar eventos, vea [Rendering Events](rendering-events.md).

Además del esquema de eventos, Windows registro de eventos también define los esquemas siguientes:

-   [Esquema eventManifest:](eventmanifestschema-schema.md)define los elementos y tipos usados para escribir un manifiesto de instrumentación.
-   [Esquema de](queryschema-schema.md)consulta: define los elementos y tipos usados para escribir una consulta para recuperar eventos de uno o varios canales.

 

 




