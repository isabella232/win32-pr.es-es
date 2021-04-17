---
title: Esquema EventManifest
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 'Más información acerca de: esquema de EventManifest'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e1c2e9b769cd26e81a71853037655220a27d1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697161"
---
# <a name="eventmanifest-schema"></a><span data-ttu-id="4542e-103">Esquema EventManifest</span><span class="sxs-lookup"><span data-stu-id="4542e-103">EventManifest Schema</span></span>

<span data-ttu-id="4542e-104">El esquema EventManifest define los siguientes elementos y tipos que se usan para escribir un manifiesto de instrumentación:</span><span class="sxs-lookup"><span data-stu-id="4542e-104">The EventManifest schema defines the following elements and types that you use to write an instrumentation manifest:</span></span>

-   [<span data-ttu-id="4542e-105">Elementos EventManifestSchema</span><span class="sxs-lookup"><span data-stu-id="4542e-105">EventManifestSchema Elements</span></span>](eventmanifestschema-elements.md)
-   [<span data-ttu-id="4542e-106">EventManifestSchema tipos simples</span><span class="sxs-lookup"><span data-stu-id="4542e-106">EventManifestSchema Simple Types</span></span>](eventmanifestschema-simple-types.md)
-   [<span data-ttu-id="4542e-107">Tipos complejos de EventManifestSchema</span><span class="sxs-lookup"><span data-stu-id="4542e-107">EventManifestSchema Complex Types</span></span>](eventmanifestschema-complex-types.md)

<span data-ttu-id="4542e-108">La sección Elements contiene los nombres de los elementos que se usan en el manifiesto; sin embargo, para obtener los detalles de cada elemento, vea el tipo complejo que contiene el elemento.</span><span class="sxs-lookup"><span data-stu-id="4542e-108">The elements section contains the names of the elements that you use in your manifest; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="4542e-109">Un manifiesto de instrumentación es un archivo XML que define un proveedor de eventos, los canales en los que se escriben los eventos, los propios eventos, los criterios de filtrado de eventos, como niveles, tareas y códigos de acceso, y las cadenas localizadas que se utilizan al representar los eventos.</span><span class="sxs-lookup"><span data-stu-id="4542e-109">An instrumentation manifest is an XML file that defines an event provider, the channels to which the events are written, the events themselves, the event filtering criteria such as levels, tasks, and opcodes, and the localized strings used when rendering the events.</span></span> <span data-ttu-id="4542e-110">La Convención es usar. man como extensión para los archivos de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="4542e-110">The convention is to use .man as the extension for manifest files.</span></span> <span data-ttu-id="4542e-111">Para obtener más información sobre cómo escribir un manifiesto, consulte [escribir un manifiesto de instrumentación](writing-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="4542e-111">For details on writing a manifest, see [Writing an Instrumentation Manifest](writing-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="4542e-112">El Windows SDK incluye el esquema en el \\ \\ archivo. xsd del evento include.</span><span class="sxs-lookup"><span data-stu-id="4542e-112">The Windows SDK includes the schema in the \\Include\\Eventman.xsd file.</span></span> <span data-ttu-id="4542e-113">Puede usar el XSD para validar el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="4542e-113">You can use the XSD to validate your manifest.</span></span>

<span data-ttu-id="4542e-114">Además del esquema EventManifest, el registro de eventos de Windows también define los esquemas siguientes:</span><span class="sxs-lookup"><span data-stu-id="4542e-114">In addition to the EventManifest schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="4542e-115">[Esquema de eventos](eventschema-schema.md): define los elementos y los tipos que se usan para representar un evento.</span><span class="sxs-lookup"><span data-stu-id="4542e-115">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>
-   <span data-ttu-id="4542e-116">[Esquema de consulta](queryschema-schema.md): define los elementos y tipos que se usan para escribir una consulta para recuperar eventos de uno o más canales.</span><span class="sxs-lookup"><span data-stu-id="4542e-116">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




