---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c6dd8ce98b071f1eb239762544a9b72160035
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721393"
---
# <a name="printcapabilities"></a><span data-ttu-id="4b11a-104">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="4b11a-104">PrintCapabilities</span></span>

<span data-ttu-id="4b11a-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="4b11a-105">This topic is not current.</span></span> <span data-ttu-id="4b11a-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4b11a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4b11a-107">Un elemento PrintCapabilities representa la raíz del documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="4b11a-107">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="4b11a-108">El documento de PrintCapabilities contiene toda la información necesaria para describir los atributos de dispositivo admitidos, dada una configuración de dispositivo concreta.</span><span class="sxs-lookup"><span data-stu-id="4b11a-108">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="4b11a-109">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="4b11a-109">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="4b11a-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="4b11a-110">XML Attributes</span></span>

<span data-ttu-id="4b11a-111">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="4b11a-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="4b11a-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="4b11a-112">XML Attribute</span></span>      | <span data-ttu-id="4b11a-113">Detalles</span><span class="sxs-lookup"><span data-stu-id="4b11a-113">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b11a-114">version</span><span class="sxs-lookup"><span data-stu-id="4b11a-114">version</span></span><br/> | <span data-ttu-id="4b11a-115">Especifica la versión del esquema que define los tipos de elemento y su estructura.</span><span class="sxs-lookup"><span data-stu-id="4b11a-115">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="4b11a-116">El atributo version es de tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="4b11a-116">The version attribute is of type integer.</span></span> <span data-ttu-id="4b11a-117">La versión del esquema actual se designa como "1".</span><span class="sxs-lookup"><span data-stu-id="4b11a-117">The current schema version is designated "1".</span></span> <span data-ttu-id="4b11a-118">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="4b11a-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="4b11a-119">Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="4b11a-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="4b11a-120">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="4b11a-120">Element Information</span></span>

<span data-ttu-id="4b11a-121">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="4b11a-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="4b11a-122">Category</span><span class="sxs-lookup"><span data-stu-id="4b11a-122">Category</span></span>                   | <span data-ttu-id="4b11a-123">Detalles</span><span class="sxs-lookup"><span data-stu-id="4b11a-123">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b11a-124">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="4b11a-124">Parent elements</span></span><br/> | <span data-ttu-id="4b11a-125">Solo raíz de documento.</span><span class="sxs-lookup"><span data-stu-id="4b11a-125">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="4b11a-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4b11a-126">Child elements</span></span><br/>  | <span data-ttu-id="4b11a-127">*Característica* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="4b11a-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="4b11a-128">*ParameterDef* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="4b11a-128">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="4b11a-129">*Propiedad* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="4b11a-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="4b11a-130">Este elemento</span><span class="sxs-lookup"><span data-stu-id="4b11a-130">This element</span></span><br/>    | <span data-ttu-id="4b11a-131">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4b11a-131">No character data is permitted.</span></span><br/> <span data-ttu-id="4b11a-132">No se permiten nodos secundarios duplicados.</span><span class="sxs-lookup"><span data-stu-id="4b11a-132">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="4b11a-133">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="4b11a-133">Configuration Dependencies</span></span>

<span data-ttu-id="4b11a-134">Es posible que el elemento raíz no tenga dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="4b11a-134">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="4b11a-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4b11a-135">Example</span></span>

<span data-ttu-id="4b11a-136">Vea [ejemplo de documento de PrintCapabilities](printcapabilities-document-example.md).</span><span class="sxs-lookup"><span data-stu-id="4b11a-136">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b11a-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4b11a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b11a-138">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4b11a-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




