---
description: Obtenga información sobre el elemento PrintCapabilities, que representa la raíz del documento PrintCapabilities.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2158fd651849df2e4ea24c640065f1041569741a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407028"
---
# <a name="printcapabilities"></a><span data-ttu-id="dac0b-103">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="dac0b-103">PrintCapabilities</span></span>

<span data-ttu-id="dac0b-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="dac0b-104">This topic is not current.</span></span> <span data-ttu-id="dac0b-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dac0b-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dac0b-106">Un elemento PrintCapabilities representa la raíz del documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="dac0b-106">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="dac0b-107">El documento PrintCapabilities contiene toda la información necesaria para describir los atributos de dispositivo admitidos, dada una configuración de dispositivo determinada.</span><span class="sxs-lookup"><span data-stu-id="dac0b-107">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="dac0b-108">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="dac0b-108">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="dac0b-109">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="dac0b-109">XML Attributes</span></span>

<span data-ttu-id="dac0b-110">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="dac0b-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="dac0b-111">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="dac0b-111">XML Attribute</span></span>      | <span data-ttu-id="dac0b-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="dac0b-112">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac0b-113">version</span><span class="sxs-lookup"><span data-stu-id="dac0b-113">version</span></span><br/> | <span data-ttu-id="dac0b-114">Especifica la versión del esquema que define los tipos de elemento y su estructura.</span><span class="sxs-lookup"><span data-stu-id="dac0b-114">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="dac0b-115">El atributo version es de tipo integer.</span><span class="sxs-lookup"><span data-stu-id="dac0b-115">The version attribute is of type integer.</span></span> <span data-ttu-id="dac0b-116">La versión del esquema actual se designa como "1".</span><span class="sxs-lookup"><span data-stu-id="dac0b-116">The current schema version is designated "1".</span></span> <span data-ttu-id="dac0b-117">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="dac0b-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="dac0b-118">Para más información, consulte la [sección Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="dac0b-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="dac0b-119">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="dac0b-119">Element Information</span></span>

<span data-ttu-id="dac0b-120">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="dac0b-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="dac0b-121">Category</span><span class="sxs-lookup"><span data-stu-id="dac0b-121">Category</span></span>                   | <span data-ttu-id="dac0b-122">Detalles</span><span class="sxs-lookup"><span data-stu-id="dac0b-122">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac0b-123">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="dac0b-123">Parent elements</span></span><br/> | <span data-ttu-id="dac0b-124">Solo raíz del documento.</span><span class="sxs-lookup"><span data-stu-id="dac0b-124">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="dac0b-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dac0b-125">Child elements</span></span><br/>  | <span data-ttu-id="dac0b-126">*Característica* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="dac0b-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="dac0b-127">*ParameterDef* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="dac0b-127">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="dac0b-128">*Propiedad* (cero o más)</span><span class="sxs-lookup"><span data-stu-id="dac0b-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="dac0b-129">Este elemento</span><span class="sxs-lookup"><span data-stu-id="dac0b-129">This element</span></span><br/>    | <span data-ttu-id="dac0b-130">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="dac0b-130">No character data is permitted.</span></span><br/> <span data-ttu-id="dac0b-131">No se permiten elementos secundarios duplicados relacionados.</span><span class="sxs-lookup"><span data-stu-id="dac0b-131">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="dac0b-132">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="dac0b-132">Configuration Dependencies</span></span>

<span data-ttu-id="dac0b-133">Es posible que el elemento raíz no tenga dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="dac0b-133">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="dac0b-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dac0b-134">Example</span></span>

<span data-ttu-id="dac0b-135">Vea [Ejemplo de documento PrintCapabilities](printcapabilities-document-example.md).</span><span class="sxs-lookup"><span data-stu-id="dac0b-135">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dac0b-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dac0b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dac0b-137">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="dac0b-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




