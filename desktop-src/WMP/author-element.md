---
title: Elemento AUTHOR
description: El elemento AUTHOR contiene el nombre del autor de un metarchivo de Windows Media o de un clip multimedia.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Elemento de autor de Windows Media Player
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698732"
---
# <a name="author-element"></a><span data-ttu-id="18e3c-104">Elemento AUTHOR</span><span class="sxs-lookup"><span data-stu-id="18e3c-104">AUTHOR Element</span></span>

<span data-ttu-id="18e3c-105">El elemento **Author** contiene el nombre del autor de un metarchivo de Windows Media o de un clip multimedia.</span><span class="sxs-lookup"><span data-stu-id="18e3c-105">The **AUTHOR** element contains the name of the author of a Windows Media metafile or media clip.</span></span>

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a><span data-ttu-id="18e3c-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="18e3c-106">Attributes</span></span>

<span data-ttu-id="18e3c-107">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="18e3c-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="18e3c-108">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="18e3c-108">Parent/Child Elements</span></span>



| <span data-ttu-id="18e3c-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="18e3c-109">Hierarchy</span></span>       | <span data-ttu-id="18e3c-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="18e3c-110">Element</span></span>            |
|-----------------|--------------------|
| <span data-ttu-id="18e3c-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="18e3c-111">Parent elements</span></span> | <span data-ttu-id="18e3c-112">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="18e3c-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="18e3c-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="18e3c-113">Child elements</span></span>  | <span data-ttu-id="18e3c-114">Ninguno</span><span class="sxs-lookup"><span data-stu-id="18e3c-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="18e3c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18e3c-115">Remarks</span></span>

<span data-ttu-id="18e3c-116">Este elemento contiene una cadena de texto que representa el nombre del autor de un metarchivo de Windows Media o un clip multimedia.</span><span class="sxs-lookup"><span data-stu-id="18e3c-116">This element contains a text string representing the name of the author of a Windows Media metafile or media clip.</span></span> <span data-ttu-id="18e3c-117">Puede usar el elemento **Author** dentro del elemento **ASX** y dentro de los elementos de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="18e3c-117">You can use the **AUTHOR** element within the **ASX** element and within **ENTRY** elements.</span></span>

<span data-ttu-id="18e3c-118">Si este elemento aparece en el elemento **ASX** , el texto se muestra como **Mostrar** información.</span><span class="sxs-lookup"><span data-stu-id="18e3c-118">If this element appears in the **ASX** element, the text is displayed as **Show** information.</span></span>

<span data-ttu-id="18e3c-119">Si este elemento aparece en un elemento de **entrada** , el texto se muestra como autor del clip.</span><span class="sxs-lookup"><span data-stu-id="18e3c-119">If this element appears in an **ENTRY** element, the text is displayed as the clip author.</span></span>

<span data-ttu-id="18e3c-120">Cada elemento **ASX** y **entry** primarios debe contener como máximo un elemento secundario **Author** .</span><span class="sxs-lookup"><span data-stu-id="18e3c-120">Each parent **ASX** and **ENTRY** element should contain at most one child **AUTHOR** element.</span></span> <span data-ttu-id="18e3c-121">Varios elementos **Author** después del primero se omitirán y no se mostrarán.</span><span class="sxs-lookup"><span data-stu-id="18e3c-121">Multiple **AUTHOR** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="18e3c-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="18e3c-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="18e3c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18e3c-123">Requirements</span></span>



| <span data-ttu-id="18e3c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="18e3c-124">Requirement</span></span> | <span data-ttu-id="18e3c-125">Value</span><span class="sxs-lookup"><span data-stu-id="18e3c-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="18e3c-126">Versión</span><span class="sxs-lookup"><span data-stu-id="18e3c-126">Version</span></span><br/> | <span data-ttu-id="18e3c-127">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="18e3c-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18e3c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="18e3c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e3c-129">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="18e3c-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="18e3c-130">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="18e3c-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





