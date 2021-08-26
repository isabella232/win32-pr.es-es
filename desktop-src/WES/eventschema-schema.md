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
ms.openlocfilehash: c08e22ad44cb1eec461ebe70361a8ee4640a7fdf5a7eb7040b2774a520be7a05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904365"
---
# <a name="event-schema"></a>Esquema de eventos

El esquema de eventos define los siguientes elementos y tipos que identifican los elementos y atributos de un evento registrado:

-   [Elementos EventSchema](eventschema-elements.md)
-   [Tipos simples de EventSchema](eventschema-simple-types.md)
-   [Tipos complejos de EventSchema](eventschema-complex-types.md)

La sección elements contiene los nombres de los elementos que encontraría en un evento registrado; sin embargo, para obtener los detalles de cada elemento, vea el tipo complejo que contiene el elemento.

El SDK Windows incluye el esquema en el \\ archivo \\ Include Event.xsd.

Puede usar este esquema para identificar los elementos y atributos al llamar a la función [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) para representar secciones o propiedades específicas del evento. Para obtener un ejemplo que muestra cómo usar este esquema al representar eventos, vea [Eventos de representación](rendering-events.md).

Además del esquema de eventos, Windows registro de eventos también define los esquemas siguientes:

-   [Esquema EventManifest:](eventmanifestschema-schema.md)define los elementos y tipos usados para escribir un manifiesto de instrumentación.
-   [Esquema de](queryschema-schema.md)consulta: define los elementos y tipos usados para escribir una consulta para recuperar eventos de uno o varios canales.

 

 




