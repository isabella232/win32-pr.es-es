---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Referencia de esquema de impresión heredado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881e986501950108c06e1e92303d13dc06265aae
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105660015"
---
# <a name="legacy-print-schema-reference"></a><span data-ttu-id="1d27f-104">Referencia de esquema de impresión heredado</span><span class="sxs-lookup"><span data-stu-id="1d27f-104">Legacy Print Schema Reference</span></span>

<span data-ttu-id="1d27f-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="1d27f-105">This topic is not current.</span></span> <span data-ttu-id="1d27f-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1d27f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1d27f-107">El esquema de impresión y las tecnologías relacionadas están disponibles en Microsoft .NET Framework 3,0, Microsoft Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1d27f-107">The Print Schema and related technologies are available in the Microsoft .NET Framework 3.0, Microsoft Windows Vista, and later releases.</span></span>

<span data-ttu-id="1d27f-108">El esquema de impresión proporciona un formato basado en XML para expresar y organizar un conjunto grande de propiedades que describen un formato de trabajo o PrintCapabilities de manera jerárquica.</span><span class="sxs-lookup"><span data-stu-id="1d27f-108">The Print Schema provides an XML-based format for expressing and organizing a large set of properties that describe either a job format or PrintCapabilities in a hierarchically structured manner.</span></span>

<span data-ttu-id="1d27f-109">El esquema de impresión es un término genérico que incluye dos componentes, las palabras clave del esquema de impresión y el marco de trabajo del esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="1d27f-109">The Print Schema is an umbrella term that includes two components, the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="1d27f-110">El documento imprimir palabras clave del esquema es un esquema público que define un conjunto de instancias de elementos que se pueden usar para describir los atributos de dispositivo y el formato de los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="1d27f-110">The Print Schema Keywords document is a public schema that defines a set of element instances that can be used to describe device attributes and print job formatting.</span></span> <span data-ttu-id="1d27f-111">El marco de trabajo de esquema de impresión es un esquema público que define una colección jerárquicamente estructurada de tipos de elementos XML y especifica cómo se pueden usar los tipos de elementos juntos.</span><span class="sxs-lookup"><span data-stu-id="1d27f-111">The Print Schema Framework is a public schema that defines a hierarchically structured collection of XML element types, and specifies how the element types can be used together.</span></span>

<span data-ttu-id="1d27f-112">Las palabras clave del esquema de impresión y el marco de esquema de impresión forman la base de dos tecnologías relacionadas con el esquema de impresión, el esquema de PrintCapabilities y el esquema de PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="1d27f-112">The Print Schema Keywords and the Print Schema Framework form the foundation for two Print Schema-related technologies, the PrintCapabilities Schema, and the PrintTicket Schema.</span></span>

<span data-ttu-id="1d27f-113">Es importante tener en cuenta que uno de los objetivos del esquema de impresión es admitir las extensiones de esquema por proveedores.</span><span class="sxs-lookup"><span data-stu-id="1d27f-113">It is important to keep in mind that one of the goals of the Print Schema is to support schema extensions by providers.</span></span> <span data-ttu-id="1d27f-114">Es decir, los proveedores no están restringidos al uso de las instancias de propiedad, característica, opción o ParameterInit definidas en las palabras clave del esquema de impresión en las tecnologías basadas en el marco de trabajo del esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="1d27f-114">That is, providers are not restricted to using only those Property, Feature, Option, or ParameterInit instances defined in the Print Schema Keywords in the technologies built on the Print Schema Framework.</span></span> <span data-ttu-id="1d27f-115">Las instancias de elementos específicas del proveedor pueden intercalarse libremente dentro de las instancias de elemento definidas en las palabras clave del esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="1d27f-115">Provider-specific element instances may be freely interspersed within element instances defined in the Print Schema Keywords.</span></span> <span data-ttu-id="1d27f-116">El único requisito es que las instancias de propiedad específicas del proveedor (es decir, privadas) deben pertenecer a un espacio de nombres que esté claramente asociado al proveedor.</span><span class="sxs-lookup"><span data-stu-id="1d27f-116">The only requirement is that provider-specific (that is, private) Property instances must belong to a namespace that is clearly associated with the provider.</span></span>

-   [<span data-ttu-id="1d27f-117">Fondo del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1d27f-117">Print Schema Background</span></span>](print-schema-background.md)

-   [<span data-ttu-id="1d27f-118">Tecnologías de Schema-Related de impresión</span><span class="sxs-lookup"><span data-stu-id="1d27f-118">Print Schema-Related Technologies</span></span>](print-schema-related-technologies.md)

-   [<span data-ttu-id="1d27f-119">Términos usados en el esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1d27f-119">Terms Used in the Print Schema</span></span>](terms-used-in-the-print-schema.md)

-   [<span data-ttu-id="1d27f-120">Sintaxis del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1d27f-120">Syntax of the Print Schema</span></span>](syntax-of-the-print-schema.md)

-   [<span data-ttu-id="1d27f-121">Resumen de tipos de elemento</span><span class="sxs-lookup"><span data-stu-id="1d27f-121">Summary of Element Types</span></span>](summary-of-element-types.md)

-   [<span data-ttu-id="1d27f-122">Marco de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1d27f-122">Print Schema Framework</span></span>](print-schema-framework.md)

-   [<span data-ttu-id="1d27f-123">Palabras clave públicas de esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1d27f-123">Print Schema Public Keywords</span></span>](print-schema-public-keywords.md)

-   [<span data-ttu-id="1d27f-124">Esquema y construcción de documentos de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="1d27f-124">PrintCapabilities Schema and Document Construction</span></span>](printcapabilities-schema-and-document-construction.md)

-   [<span data-ttu-id="1d27f-125">Esquema PrintTicket y construcción de documentos</span><span class="sxs-lookup"><span data-stu-id="1d27f-125">PrintTicket Schema and Document Construction</span></span>](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a><span data-ttu-id="1d27f-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d27f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d27f-127">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="1d27f-127">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



