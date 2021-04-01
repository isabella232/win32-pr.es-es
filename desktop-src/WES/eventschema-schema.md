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
# <a name="event-schema"></a><span data-ttu-id="dc722-103">Esquema de eventos</span><span class="sxs-lookup"><span data-stu-id="dc722-103">Event Schema</span></span>

<span data-ttu-id="dc722-104">El esquema de eventos define los siguientes elementos y tipos que identifican los elementos y los atributos de un evento registrado:</span><span class="sxs-lookup"><span data-stu-id="dc722-104">The Event schema defines the following elements and types that identify the elements and attributes of a logged event:</span></span>

-   [<span data-ttu-id="dc722-105">Elementos EventSchema</span><span class="sxs-lookup"><span data-stu-id="dc722-105">EventSchema Elements</span></span>](eventschema-elements.md)
-   [<span data-ttu-id="dc722-106">EventSchema tipos simples</span><span class="sxs-lookup"><span data-stu-id="dc722-106">EventSchema Simple Types</span></span>](eventschema-simple-types.md)
-   [<span data-ttu-id="dc722-107">Tipos complejos de EventSchema</span><span class="sxs-lookup"><span data-stu-id="dc722-107">EventSchema Complex Types</span></span>](eventschema-complex-types.md)

<span data-ttu-id="dc722-108">La sección Elements contiene los nombres de los elementos que encontraría en los eventos registrados; sin embargo, para obtener los detalles de cada elemento, vea el tipo complejo que contiene el elemento.</span><span class="sxs-lookup"><span data-stu-id="dc722-108">The elements section contains the names of the elements that you would find in a logged events; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="dc722-109">El Windows SDK incluye el esquema en el \\ \\ archivo Event. xsd de inclusión.</span><span class="sxs-lookup"><span data-stu-id="dc722-109">The Windows SDK includes the schema in the \\Include\\Event.xsd file.</span></span>

<span data-ttu-id="dc722-110">Puede utilizar este esquema para identificar los elementos y atributos al llamar a la función [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) para representar secciones o propiedades específicas del evento.</span><span class="sxs-lookup"><span data-stu-id="dc722-110">You can use this schema to identify the elements and attributes when calling the [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function to render specific sections or properties of the event.</span></span> <span data-ttu-id="dc722-111">Para obtener un ejemplo en el que se muestra cómo usar este esquema al representar eventos, vea [representar eventos](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="dc722-111">For an example that shows how to use this schema when rendering events, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="dc722-112">Además del esquema de eventos, el registro de eventos de Windows también define los esquemas siguientes:</span><span class="sxs-lookup"><span data-stu-id="dc722-112">In addition to the Event schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="dc722-113">[Esquema EventManifest](eventmanifestschema-schema.md): define los elementos y tipos que se usan para escribir un manifiesto de instrumentación.</span><span class="sxs-lookup"><span data-stu-id="dc722-113">[EventManifest Schema](eventmanifestschema-schema.md)—defines the elements and types used to write an instrumentation manifest.</span></span>
-   <span data-ttu-id="dc722-114">[Esquema de consulta](queryschema-schema.md): define los elementos y tipos que se usan para escribir una consulta para recuperar eventos de uno o más canales.</span><span class="sxs-lookup"><span data-stu-id="dc722-114">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




