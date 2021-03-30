---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cb985e746b400b1c804f21b5996352ae590e3b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279867"
---
# <a name="parameterinit"></a><span data-ttu-id="71c24-104">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="71c24-104">ParameterInit</span></span>

<span data-ttu-id="71c24-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="71c24-105">This topic is not current.</span></span> <span data-ttu-id="71c24-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="71c24-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="71c24-107">Define un valor para una instancia de un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="71c24-107">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="71c24-108">Un elemento ParameterInit es el destino de la referencia realizada por un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="71c24-108">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="71c24-109">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="71c24-109">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="71c24-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="71c24-110">XML Attributes</span></span>

<span data-ttu-id="71c24-111">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="71c24-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="71c24-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="71c24-112">XML Attribute</span></span>   | <span data-ttu-id="71c24-113">Detalles</span><span class="sxs-lookup"><span data-stu-id="71c24-113">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71c24-114">name</span><span class="sxs-lookup"><span data-stu-id="71c24-114">name</span></span><br/> | <span data-ttu-id="71c24-115">Contiene el atributo name del elemento ParameterDef que se va a inicializar en el contexto del documento actual.</span><span class="sxs-lookup"><span data-stu-id="71c24-115">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="71c24-116">Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="71c24-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="71c24-117">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="71c24-117">Element Information</span></span>

<span data-ttu-id="71c24-118">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="71c24-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="71c24-119">Category</span><span class="sxs-lookup"><span data-stu-id="71c24-119">Category</span></span>                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71c24-120">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="71c24-120">Parent elements</span></span><br/> | <span data-ttu-id="71c24-121">PrintTicket (raíz de PrintTicket)</span><span class="sxs-lookup"><span data-stu-id="71c24-121">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="71c24-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="71c24-122">Child elements</span></span><br/>  | <span data-ttu-id="71c24-123">Valor (uno)</span><span class="sxs-lookup"><span data-stu-id="71c24-123">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="71c24-124">Este elemento</span><span class="sxs-lookup"><span data-stu-id="71c24-124">This element</span></span><br/>    | <span data-ttu-id="71c24-125">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="71c24-125">No character data is permitted.</span></span><br/> <span data-ttu-id="71c24-126">No se permiten nodos secundarios duplicados.</span><span class="sxs-lookup"><span data-stu-id="71c24-126">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="71c24-127">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="71c24-127">Configuration Dependencies</span></span>

<span data-ttu-id="71c24-128">None</span><span class="sxs-lookup"><span data-stu-id="71c24-128">None</span></span>

## <a name="example"></a><span data-ttu-id="71c24-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71c24-129">Example</span></span>

<span data-ttu-id="71c24-130">En el ejemplo siguiente se inicializa un parámetro en 1.</span><span class="sxs-lookup"><span data-stu-id="71c24-130">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="71c24-131">En el ejemplo de [ParameterDef](parameterdef.md) se muestra cómo establecer todos los elementos de propiedad necesarios para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="71c24-131">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="71c24-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="71c24-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71c24-133">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="71c24-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




