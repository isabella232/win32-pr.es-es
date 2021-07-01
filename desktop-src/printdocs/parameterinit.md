---
description: Obtenga información sobre el elemento ParameterInit, que define un valor para una instancia de un elemento ParameterDef.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0e0cadbf26d6ff516ab0ace90165e11420a9b7
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118980"
---
# <a name="parameterinit"></a><span data-ttu-id="b9609-103">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="b9609-103">ParameterInit</span></span>

<span data-ttu-id="b9609-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="b9609-104">This topic is not current.</span></span> <span data-ttu-id="b9609-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b9609-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b9609-106">Define un valor para una instancia de un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="b9609-106">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="b9609-107">Un elemento ParameterInit es el destino de la referencia realizada por un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="b9609-107">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="b9609-108">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="b9609-108">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="b9609-109">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="b9609-109">XML Attributes</span></span>

<span data-ttu-id="b9609-110">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="b9609-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="b9609-111">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="b9609-111">XML Attribute</span></span>   | <span data-ttu-id="b9609-112">Detalles</span><span class="sxs-lookup"><span data-stu-id="b9609-112">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9609-113">name</span><span class="sxs-lookup"><span data-stu-id="b9609-113">name</span></span><br/> | <span data-ttu-id="b9609-114">Contiene el atributo name del elemento ParameterDef que se va a inicializar en el contexto del documento actual.</span><span class="sxs-lookup"><span data-stu-id="b9609-114">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="b9609-115">Para más información, consulte la [sección Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="b9609-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="b9609-116">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b9609-116">Element Information</span></span>

<span data-ttu-id="b9609-117">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="b9609-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="b9609-118">Category</span><span class="sxs-lookup"><span data-stu-id="b9609-118">Category</span></span>                   | <span data-ttu-id="b9609-119">Nombre o restricción</span><span class="sxs-lookup"><span data-stu-id="b9609-119">Name or restriction</span></span>                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9609-120">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b9609-120">Parent elements</span></span><br/> | <span data-ttu-id="b9609-121">PrintTicket (raíz de PrintTicket)</span><span class="sxs-lookup"><span data-stu-id="b9609-121">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="b9609-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b9609-122">Child elements</span></span><br/>  | <span data-ttu-id="b9609-123">Valor (uno)</span><span class="sxs-lookup"><span data-stu-id="b9609-123">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="b9609-124">Este elemento</span><span class="sxs-lookup"><span data-stu-id="b9609-124">This element</span></span><br/>    | <span data-ttu-id="b9609-125">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b9609-125">No character data is permitted.</span></span><br/> <span data-ttu-id="b9609-126">No se permiten elementos secundarios duplicados relacionados.</span><span class="sxs-lookup"><span data-stu-id="b9609-126">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="b9609-127">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="b9609-127">Configuration Dependencies</span></span>

<span data-ttu-id="b9609-128">None</span><span class="sxs-lookup"><span data-stu-id="b9609-128">None</span></span>

## <a name="example"></a><span data-ttu-id="b9609-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9609-129">Example</span></span>

<span data-ttu-id="b9609-130">En el ejemplo siguiente se inicializa un parámetro en 1.</span><span class="sxs-lookup"><span data-stu-id="b9609-130">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="b9609-131">En el ejemplo [de ParameterDef](parameterdef.md) se muestra cómo establecer todos los elementos Property necesarios para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="b9609-131">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="b9609-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9609-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9609-133">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="b9609-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




