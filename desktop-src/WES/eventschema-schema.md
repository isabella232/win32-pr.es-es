---
title: Esquema de eventos
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: 'Más información acerca de: esquema de eventos'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bfb26f6c71d544e0c0a6a4d833b40a5d15ae5485
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909597"
---
# <a name="event-schema"></a>Esquema de eventos

El esquema de eventos define los siguientes elementos y tipos que identifican los elementos y los atributos de un evento registrado:

-   [Elementos EventSchema](eventschema-elements.md)
-   [EventSchema tipos simples](eventschema-simple-types.md)
-   [Tipos complejos de EventSchema](eventschema-complex-types.md)

La sección Elements contiene los nombres de los elementos que encontraría en los eventos registrados; sin embargo, para obtener los detalles de cada elemento, vea el tipo complejo que contiene el elemento.

El Windows SDK incluye el esquema en el \\ \\ archivo Event. xsd de inclusión.

Puede utilizar este esquema para identificar los elementos y atributos al llamar a la función [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) para representar secciones o propiedades específicas del evento. Para obtener un ejemplo en el que se muestra cómo usar este esquema al representar eventos, vea [representar eventos](rendering-events.md).

Además del esquema de eventos, el registro de eventos de Windows también define los esquemas siguientes:

-   [Esquema EventManifest](eventmanifestschema-schema.md): define los elementos y tipos que se usan para escribir un manifiesto de instrumentación.
-   [Esquema de consulta](queryschema-schema.md): define los elementos y tipos que se usan para escribir una consulta para recuperar eventos de uno o más canales.

 

 




