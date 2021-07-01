---
description: Busque información sobre el elemento PrintTicket. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b279ff681704a63f6547738c73fb9192d6f8a65d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120080"
---
# <a name="printticket"></a><span data-ttu-id="12f11-105">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="12f11-105">PrintTicket</span></span>

<span data-ttu-id="12f11-106">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="12f11-106">This topic is not current.</span></span> <span data-ttu-id="12f11-107">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="12f11-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="12f11-108">Un elemento PrintTicket es el elemento raíz del documento PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="12f11-108">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="12f11-109">Un elemento PrintTicket contiene toda la información de formato de trabajo necesaria para generar un trabajo.</span><span class="sxs-lookup"><span data-stu-id="12f11-109">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="12f11-110">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="12f11-110">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="12f11-111">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="12f11-111">XML Attributes</span></span>

<span data-ttu-id="12f11-112">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="12f11-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="12f11-113">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="12f11-113">XML Attribute</span></span>      | <span data-ttu-id="12f11-114">Detalles</span><span class="sxs-lookup"><span data-stu-id="12f11-114">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f11-115">version</span><span class="sxs-lookup"><span data-stu-id="12f11-115">version</span></span><br/> | <span data-ttu-id="12f11-116">Especifica la versión del esquema que define los tipos de elemento y su estructura, un literal de tipo entero.</span><span class="sxs-lookup"><span data-stu-id="12f11-116">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="12f11-117">La versión del esquema actual es "1".</span><span class="sxs-lookup"><span data-stu-id="12f11-117">The current schema version is "1".</span></span> <span data-ttu-id="12f11-118">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="12f11-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="12f11-119">Para más información, consulte la [sección Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="12f11-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="12f11-120">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="12f11-120">Element Information</span></span>

<span data-ttu-id="12f11-121">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="12f11-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="12f11-122">Category</span><span class="sxs-lookup"><span data-stu-id="12f11-122">Category</span></span>                   | <span data-ttu-id="12f11-123">Detalles</span><span class="sxs-lookup"><span data-stu-id="12f11-123">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f11-124">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="12f11-124">Parent elements</span></span><br/> | <span data-ttu-id="12f11-125">Solo raíz del documento.</span><span class="sxs-lookup"><span data-stu-id="12f11-125">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="12f11-126">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="12f11-126">Child elements</span></span><br/>  | <span data-ttu-id="12f11-127">*Característica* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="12f11-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="12f11-128">*ParameterInit* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="12f11-128">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="12f11-129">*Propiedad* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="12f11-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="12f11-130">Este elemento</span><span class="sxs-lookup"><span data-stu-id="12f11-130">This element</span></span><br/>    | <span data-ttu-id="12f11-131">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="12f11-131">No character data is permitted.</span></span><br/> <span data-ttu-id="12f11-132">No se permiten elementos secundarios duplicados relacionados.</span><span class="sxs-lookup"><span data-stu-id="12f11-132">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="12f11-133">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="12f11-133">Configuration Dependencies</span></span>

<span data-ttu-id="12f11-134">Las dependencias de configuración solo se aplican a los elementos de un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="12f11-134">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="12f11-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="12f11-135">Example</span></span>

<span data-ttu-id="12f11-136">Vea [Ejemplo de PrintTicket.](printticket-example.md)</span><span class="sxs-lookup"><span data-stu-id="12f11-136">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12f11-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="12f11-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12f11-138">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="12f11-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




