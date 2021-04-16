---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d2e225eb38584e290db55c33594be80d0d7999
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689704"
---
# <a name="printticket"></a><span data-ttu-id="02c5c-104">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="02c5c-104">PrintTicket</span></span>

<span data-ttu-id="02c5c-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="02c5c-105">This topic is not current.</span></span> <span data-ttu-id="02c5c-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="02c5c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="02c5c-107">Un elemento PrintTicket es el elemento raíz del documento PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="02c5c-107">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="02c5c-108">Un elemento PrintTicket contiene toda la información de formato del trabajo necesaria para generar un trabajo.</span><span class="sxs-lookup"><span data-stu-id="02c5c-108">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="02c5c-109">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="02c5c-109">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="02c5c-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="02c5c-110">XML Attributes</span></span>

<span data-ttu-id="02c5c-111">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="02c5c-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="02c5c-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="02c5c-112">XML Attribute</span></span>      | <span data-ttu-id="02c5c-113">Detalles</span><span class="sxs-lookup"><span data-stu-id="02c5c-113">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02c5c-114">version</span><span class="sxs-lookup"><span data-stu-id="02c5c-114">version</span></span><br/> | <span data-ttu-id="02c5c-115">Especifica la versión del esquema que define los tipos de elemento y su estructura, un literal de tipo entero.</span><span class="sxs-lookup"><span data-stu-id="02c5c-115">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="02c5c-116">La versión del esquema actual es "1".</span><span class="sxs-lookup"><span data-stu-id="02c5c-116">The current schema version is "1".</span></span> <span data-ttu-id="02c5c-117">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="02c5c-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="02c5c-118">Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="02c5c-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="02c5c-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="02c5c-119">Element Information</span></span>

<span data-ttu-id="02c5c-120">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="02c5c-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="02c5c-121">Category</span><span class="sxs-lookup"><span data-stu-id="02c5c-121">Category</span></span>                   | <span data-ttu-id="02c5c-122">Detalles</span><span class="sxs-lookup"><span data-stu-id="02c5c-122">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02c5c-123">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="02c5c-123">Parent elements</span></span><br/> | <span data-ttu-id="02c5c-124">Solo raíz de documento.</span><span class="sxs-lookup"><span data-stu-id="02c5c-124">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="02c5c-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="02c5c-125">Child elements</span></span><br/>  | <span data-ttu-id="02c5c-126">*Característica* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="02c5c-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="02c5c-127">*ParameterInit* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="02c5c-127">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="02c5c-128">*Propiedad* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="02c5c-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="02c5c-129">Este elemento</span><span class="sxs-lookup"><span data-stu-id="02c5c-129">This element</span></span><br/>    | <span data-ttu-id="02c5c-130">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="02c5c-130">No character data is permitted.</span></span><br/> <span data-ttu-id="02c5c-131">No se permiten nodos secundarios duplicados.</span><span class="sxs-lookup"><span data-stu-id="02c5c-131">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="02c5c-132">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="02c5c-132">Configuration Dependencies</span></span>

<span data-ttu-id="02c5c-133">Las dependencias de configuración solo se pueden aplicar a los elementos de un documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="02c5c-133">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="02c5c-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="02c5c-134">Example</span></span>

<span data-ttu-id="02c5c-135">Vea el [ejemplo de PrintTicket](printticket-example.md).</span><span class="sxs-lookup"><span data-stu-id="02c5c-135">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02c5c-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02c5c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02c5c-137">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="02c5c-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




