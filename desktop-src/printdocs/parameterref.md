---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2ef6655439718c1038afe2d342910c54db45ba
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717421"
---
# <a name="parameterref"></a><span data-ttu-id="d50ed-104">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="d50ed-104">ParameterRef</span></span>

<span data-ttu-id="d50ed-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="d50ed-105">This topic is not current.</span></span> <span data-ttu-id="d50ed-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d50ed-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d50ed-107">Un elemento ParameterRef define una referencia a un elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="d50ed-107">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="d50ed-108">Un elemento ScoredProperty que contiene un elemento ParameterRef no tiene un elemento de valor establecido explícitamente.</span><span class="sxs-lookup"><span data-stu-id="d50ed-108">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="d50ed-109">En su lugar, el elemento ScoredProperty recibe su valor del elemento ParameterInit al que hace referencia un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="d50ed-109">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="d50ed-110">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="d50ed-110">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="d50ed-111">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="d50ed-111">XML Attributes</span></span>

<span data-ttu-id="d50ed-112">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="d50ed-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="d50ed-113">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="d50ed-113">XML Attribute</span></span>   | <span data-ttu-id="d50ed-114">Detalles</span><span class="sxs-lookup"><span data-stu-id="d50ed-114">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d50ed-115">name</span><span class="sxs-lookup"><span data-stu-id="d50ed-115">name</span></span><br/> | <span data-ttu-id="d50ed-116">Contiene el atributo name del elemento ParameterDef al que se hace referencia en el contexto del documento actual.</span><span class="sxs-lookup"><span data-stu-id="d50ed-116">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="d50ed-117">Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="d50ed-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="d50ed-118">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d50ed-118">Element Information</span></span>

<span data-ttu-id="d50ed-119">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="d50ed-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="d50ed-120">Category</span><span class="sxs-lookup"><span data-stu-id="d50ed-120">Category</span></span>                   | <span data-ttu-id="d50ed-121">Detalles</span><span class="sxs-lookup"><span data-stu-id="d50ed-121">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d50ed-122">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="d50ed-122">Parent elements</span></span><br/> | <span data-ttu-id="d50ed-123">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="d50ed-123">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="d50ed-124">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d50ed-124">Child elements</span></span><br/>  | <span data-ttu-id="d50ed-125">Ninguno permitido.</span><span class="sxs-lookup"><span data-stu-id="d50ed-125">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="d50ed-126">Este elemento</span><span class="sxs-lookup"><span data-stu-id="d50ed-126">This element</span></span><br/>    | <span data-ttu-id="d50ed-127">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d50ed-127">No character data is permitted.</span></span><br/> <span data-ttu-id="d50ed-128">No se permiten nodos secundarios duplicados.</span><span class="sxs-lookup"><span data-stu-id="d50ed-128">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="d50ed-129">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="d50ed-129">Configuration Dependencies</span></span>

<span data-ttu-id="d50ed-130">Los elementos ParameterRef no pueden tener dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="d50ed-130">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="d50ed-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d50ed-131">Example</span></span>

<span data-ttu-id="d50ed-132">En el ejemplo siguiente se muestra cómo usar los elementos ParameterRef para permitir que los usuarios escriban parámetros de tamaño multimedia personalizados.</span><span class="sxs-lookup"><span data-stu-id="d50ed-132">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a><span data-ttu-id="d50ed-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d50ed-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d50ed-134">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d50ed-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




