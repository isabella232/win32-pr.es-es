---
title: Elemento ABSTRACT
description: El elemento ABSTRACTo contiene texto que describe el elemento ASX, BANNER o ENTRY asociado.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Media Player de elementos ABSTRACTos de Windows
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699992"
---
# <a name="abstract-element"></a><span data-ttu-id="0edfb-104">Elemento ABSTRACT</span><span class="sxs-lookup"><span data-stu-id="0edfb-104">ABSTRACT Element</span></span>

<span data-ttu-id="0edfb-105">El elemento **abstracto** contiene texto que describe el elemento **ASX**, **banner** o **entry** asociado.</span><span class="sxs-lookup"><span data-stu-id="0edfb-105">The **ABSTRACT** element contains text that describes the associated **ASX**, **BANNER**, or **ENTRY** element.</span></span>

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a><span data-ttu-id="0edfb-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="0edfb-106">Attributes</span></span>

<span data-ttu-id="0edfb-107">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="0edfb-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="0edfb-108">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="0edfb-108">Parent/Child Elements</span></span>



| <span data-ttu-id="0edfb-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="0edfb-109">Hierarchy</span></span> | <span data-ttu-id="0edfb-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="0edfb-110">Elements</span></span>                       |
|-----------|--------------------------------|
| <span data-ttu-id="0edfb-111">Parent</span><span class="sxs-lookup"><span data-stu-id="0edfb-111">Parent</span></span>    | <span data-ttu-id="0edfb-112">**ASX**, **entrada**, **banner**</span><span class="sxs-lookup"><span data-stu-id="0edfb-112">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="0edfb-113">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="0edfb-113">Child</span></span>     | <span data-ttu-id="0edfb-114">None</span><span class="sxs-lookup"><span data-stu-id="0edfb-114">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="0edfb-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0edfb-115">Remarks</span></span>

<span data-ttu-id="0edfb-116">Si este elemento aparece dentro de un elemento **ASX** , el texto se muestra como información sobre herramientas cuando se mantiene el mouse sobre el título.</span><span class="sxs-lookup"><span data-stu-id="0edfb-116">If this element appears within an **ASX** element, the text displays as a ToolTip when the mouse hovers over the show title.</span></span>

<span data-ttu-id="0edfb-117">Si este elemento aparece dentro de un elemento de **entrada** , el texto se muestra como información sobre herramientas cuando se mantiene el mouse sobre el título del clip.</span><span class="sxs-lookup"><span data-stu-id="0edfb-117">If this element appears within an **ENTRY** element, the text displays as a ToolTip when the mouse hovers over the clip title.</span></span>

<span data-ttu-id="0edfb-118">Si este elemento aparece dentro de un elemento **banner** , el texto se muestra como información sobre herramientas para el gráfico de banner.</span><span class="sxs-lookup"><span data-stu-id="0edfb-118">If this element appears within a **BANNER** element, the text displays as a ToolTip for the banner graphic.</span></span>

<span data-ttu-id="0edfb-119">Use solo un elemento **abstracto** por ámbito.</span><span class="sxs-lookup"><span data-stu-id="0edfb-119">Use only one **ABSTRACT** element per scope.</span></span> <span data-ttu-id="0edfb-120">Solo se utiliza el primer elemento **abstracto** dentro del ámbito de otro elemento cuando se procesa un archivo de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="0edfb-120">Only the first **ABSTRACT** element within the scope of another element is used when a metafile file is processed.</span></span> <span data-ttu-id="0edfb-121">Se omiten los elementos **abstractos** subsiguientes de ese ámbito.</span><span class="sxs-lookup"><span data-stu-id="0edfb-121">Any subsequent **ABSTRACT** elements in that scope are ignored.</span></span>

## <a name="examples"></a><span data-ttu-id="0edfb-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0edfb-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="0edfb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0edfb-123">Requirements</span></span>



| <span data-ttu-id="0edfb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0edfb-124">Requirement</span></span> | <span data-ttu-id="0edfb-125">Value</span><span class="sxs-lookup"><span data-stu-id="0edfb-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="0edfb-126">Versión</span><span class="sxs-lookup"><span data-stu-id="0edfb-126">Version</span></span><br/> | <span data-ttu-id="0edfb-127">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="0edfb-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0edfb-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0edfb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0edfb-129">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0edfb-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="0edfb-130">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0edfb-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





