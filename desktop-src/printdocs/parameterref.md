---
description: Obtenga información sobre el elemento ParameterRef, que define una referencia a un elemento ParameterInit y cómo funciona con ScoredProperty.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff3b0e16f53e8399a5bbbb5974a05fd6886cdd2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407188"
---
# <a name="parameterref"></a><span data-ttu-id="d695c-103">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="d695c-103">ParameterRef</span></span>

<span data-ttu-id="d695c-104">Este tema no es actual.</span><span class="sxs-lookup"><span data-stu-id="d695c-104">This topic is not current.</span></span> <span data-ttu-id="d695c-105">Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d695c-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d695c-106">Un elemento ParameterRef define una referencia a un elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="d695c-106">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="d695c-107">Un elemento ScoredProperty que contiene un elemento ParameterRef no tiene un elemento Value establecido explícitamente.</span><span class="sxs-lookup"><span data-stu-id="d695c-107">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="d695c-108">En su lugar, el elemento ScoredProperty recibe su valor del elemento ParameterInit al que hace referencia un elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="d695c-108">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="d695c-109">Etiqueta de elemento</span><span class="sxs-lookup"><span data-stu-id="d695c-109">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="d695c-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="d695c-110">XML Attributes</span></span>

<span data-ttu-id="d695c-111">En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.</span><span class="sxs-lookup"><span data-stu-id="d695c-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="d695c-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="d695c-112">XML Attribute</span></span>   | <span data-ttu-id="d695c-113">Detalles</span><span class="sxs-lookup"><span data-stu-id="d695c-113">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d695c-114">name</span><span class="sxs-lookup"><span data-stu-id="d695c-114">name</span></span><br/> | <span data-ttu-id="d695c-115">Contiene el atributo name del elemento ParameterDef al que se hace referencia en el contexto del documento actual.</span><span class="sxs-lookup"><span data-stu-id="d695c-115">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="d695c-116">Para más información, consulte la [sección Atributos XML.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="d695c-116">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="d695c-117">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="d695c-117">Element Information</span></span>

<span data-ttu-id="d695c-118">En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.</span><span class="sxs-lookup"><span data-stu-id="d695c-118">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="d695c-119">Category</span><span class="sxs-lookup"><span data-stu-id="d695c-119">Category</span></span>                   | <span data-ttu-id="d695c-120">Detalles</span><span class="sxs-lookup"><span data-stu-id="d695c-120">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d695c-121">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="d695c-121">Parent elements</span></span><br/> | <span data-ttu-id="d695c-122">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="d695c-122">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="d695c-123">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d695c-123">Child elements</span></span><br/>  | <span data-ttu-id="d695c-124">No se permite ninguna.</span><span class="sxs-lookup"><span data-stu-id="d695c-124">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="d695c-125">Este elemento</span><span class="sxs-lookup"><span data-stu-id="d695c-125">This element</span></span><br/>    | <span data-ttu-id="d695c-126">No se permiten datos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d695c-126">No character data is permitted.</span></span><br/> <span data-ttu-id="d695c-127">No se permiten elementos secundarios duplicados relacionados.</span><span class="sxs-lookup"><span data-stu-id="d695c-127">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="d695c-128">Dependencias de configuración</span><span class="sxs-lookup"><span data-stu-id="d695c-128">Configuration Dependencies</span></span>

<span data-ttu-id="d695c-129">Es posible que los elementos ParameterRef no tengan dependencias de configuración.</span><span class="sxs-lookup"><span data-stu-id="d695c-129">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="d695c-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d695c-130">Example</span></span>

<span data-ttu-id="d695c-131">En el ejemplo siguiente se muestra cómo usar elementos ParameterRef para permitir que los usuarios escriban parámetros de tamaño multimedia personalizados.</span><span class="sxs-lookup"><span data-stu-id="d695c-131">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="d695c-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d695c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d695c-133">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="d695c-133">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




