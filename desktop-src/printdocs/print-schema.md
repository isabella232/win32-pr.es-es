---
description: En esta introducción se describen los temas de referencia Esquema de impresión y vínculos a Esquema de impresión. El esquema de impresión incluye las palabras clave de esquema de impresión y el marco de trabajo.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Referencia de esquema de impresión heredado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a8f417d20913563cfd4a52ba51d21b516e73f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407138"
---
# <a name="legacy-print-schema-reference"></a><span data-ttu-id="23ce9-104">Referencia de esquema de impresión heredado</span><span class="sxs-lookup"><span data-stu-id="23ce9-104">Legacy Print Schema Reference</span></span>

<span data-ttu-id="23ce9-105">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="23ce9-105">This topic is not current.</span></span> <span data-ttu-id="23ce9-106">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="23ce9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="23ce9-107">El esquema de impresión y las tecnologías relacionadas están disponibles en Microsoft .NET Framework 3.0, Microsoft Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="23ce9-107">The Print Schema and related technologies are available in the Microsoft .NET Framework 3.0, Microsoft Windows Vista, and later releases.</span></span>

<span data-ttu-id="23ce9-108">El esquema de impresión proporciona un formato basado en XML para expresar y organizar un gran conjunto de propiedades que describen un formato de trabajo o PrintCapabilities de una manera jerárquicamente estructurada.</span><span class="sxs-lookup"><span data-stu-id="23ce9-108">The Print Schema provides an XML-based format for expressing and organizing a large set of properties that describe either a job format or PrintCapabilities in a hierarchically structured manner.</span></span>

<span data-ttu-id="23ce9-109">El esquema de impresión es un término paraguas que incluye dos componentes, las palabras clave de esquema de impresión y el marco de esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="23ce9-109">The Print Schema is an umbrella term that includes two components, the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="23ce9-110">El documento Palabras clave de esquema de impresión es un esquema público que define un conjunto de instancias de elemento que se pueden usar para describir los atributos del dispositivo y el formato del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="23ce9-110">The Print Schema Keywords document is a public schema that defines a set of element instances that can be used to describe device attributes and print job formatting.</span></span> <span data-ttu-id="23ce9-111">Print Schema Framework es un esquema público que define una colección jerárquicamente estructurada de tipos de elementos XML y especifica cómo se pueden usar conjuntamente los tipos de elemento.</span><span class="sxs-lookup"><span data-stu-id="23ce9-111">The Print Schema Framework is a public schema that defines a hierarchically structured collection of XML element types, and specifies how the element types can be used together.</span></span>

<span data-ttu-id="23ce9-112">Las palabras clave de esquema de impresión y el marco de esquema de impresión forman la base de dos tecnologías relacionadas con el esquema de impresión, el esquema PrintCapabilities y el esquema PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="23ce9-112">The Print Schema Keywords and the Print Schema Framework form the foundation for two Print Schema-related technologies, the PrintCapabilities Schema, and the PrintTicket Schema.</span></span>

<span data-ttu-id="23ce9-113">Es importante tener en cuenta que uno de los objetivos del esquema de impresión es admitir las extensiones de esquema por parte de los proveedores.</span><span class="sxs-lookup"><span data-stu-id="23ce9-113">It is important to keep in mind that one of the goals of the Print Schema is to support schema extensions by providers.</span></span> <span data-ttu-id="23ce9-114">Es decir, los proveedores no están restringidos a usar solo las instancias property, feature, option o ParameterInit definidas en las palabras clave de esquema de impresión en las tecnologías creadas en el marco de esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="23ce9-114">That is, providers are not restricted to using only those Property, Feature, Option, or ParameterInit instances defined in the Print Schema Keywords in the technologies built on the Print Schema Framework.</span></span> <span data-ttu-id="23ce9-115">Las instancias de elementos específicas del proveedor se pueden intercalar libremente dentro de las instancias de elemento definidas en las palabras clave de esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="23ce9-115">Provider-specific element instances may be freely interspersed within element instances defined in the Print Schema Keywords.</span></span> <span data-ttu-id="23ce9-116">El único requisito es que las instancias de propiedad específicas del proveedor (es decir, privadas) deben pertenecer a un espacio de nombres que esté claramente asociado al proveedor.</span><span class="sxs-lookup"><span data-stu-id="23ce9-116">The only requirement is that provider-specific (that is, private) Property instances must belong to a namespace that is clearly associated with the provider.</span></span>

-   [<span data-ttu-id="23ce9-117">Fondo del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="23ce9-117">Print Schema Background</span></span>](print-schema-background.md)

-   [<span data-ttu-id="23ce9-118">Tecnologías de Schema-Related impresión</span><span class="sxs-lookup"><span data-stu-id="23ce9-118">Print Schema-Related Technologies</span></span>](print-schema-related-technologies.md)

-   [<span data-ttu-id="23ce9-119">Términos usados en el esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="23ce9-119">Terms Used in the Print Schema</span></span>](terms-used-in-the-print-schema.md)

-   [<span data-ttu-id="23ce9-120">Sintaxis del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="23ce9-120">Syntax of the Print Schema</span></span>](syntax-of-the-print-schema.md)

-   [<span data-ttu-id="23ce9-121">Resumen de los tipos de elemento</span><span class="sxs-lookup"><span data-stu-id="23ce9-121">Summary of Element Types</span></span>](summary-of-element-types.md)

-   [<span data-ttu-id="23ce9-122">Marco de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="23ce9-122">Print Schema Framework</span></span>](print-schema-framework.md)

-   [<span data-ttu-id="23ce9-123">Palabras clave públicas del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="23ce9-123">Print Schema Public Keywords</span></span>](print-schema-public-keywords.md)

-   [<span data-ttu-id="23ce9-124">Esquema PrintCapabilities y construcción de documentos</span><span class="sxs-lookup"><span data-stu-id="23ce9-124">PrintCapabilities Schema and Document Construction</span></span>](printcapabilities-schema-and-document-construction.md)

-   [<span data-ttu-id="23ce9-125">Esquema PrintTicket y construcción de documentos</span><span class="sxs-lookup"><span data-stu-id="23ce9-125">PrintTicket Schema and Document Construction</span></span>](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a><span data-ttu-id="23ce9-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="23ce9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23ce9-127">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="23ce9-127">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



