---
title: Elemento REPEAT
description: El elemento REPEAT define el número de veces que Windows Media Player repetirá uno o varios elementos ENTRYREF o ENTRY.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- Ventanas de elementos de repetición Media Player
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650049"
---
# <a name="repeat-element"></a><span data-ttu-id="19179-104">Elemento REPEAT</span><span class="sxs-lookup"><span data-stu-id="19179-104">REPEAT Element</span></span>

<span data-ttu-id="19179-105">El elemento **REPEAT** define el número de veces que Windows Media Player repetirá uno o varios elementos **ENTRYREF** o **entry** .</span><span class="sxs-lookup"><span data-stu-id="19179-105">The **REPEAT** element defines the number of times Windows Media Player repeats one or more **ENTRY** or **ENTRYREF** elements.</span></span>

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a><span data-ttu-id="19179-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="19179-106">Attributes</span></span>

<span data-ttu-id="19179-107">**COUNT**</span><span class="sxs-lookup"><span data-stu-id="19179-107">**COUNT**</span></span>

<span data-ttu-id="19179-108">Entero que representa el número de veces que Windows Media Player repite los elementos **entry** y **ENTRYREF** dentro del ámbito de este elemento.</span><span class="sxs-lookup"><span data-stu-id="19179-108">Integer representing the number of times Windows Media Player repeats the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="19179-109">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="19179-109">Parent/Child Elements</span></span>



| <span data-ttu-id="19179-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="19179-110">Hierarchy</span></span>       | <span data-ttu-id="19179-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="19179-111">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="19179-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="19179-112">Parent elements</span></span> | <span data-ttu-id="19179-113">**ASX**</span><span class="sxs-lookup"><span data-stu-id="19179-113">**ASX**</span></span>                 |
| <span data-ttu-id="19179-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="19179-114">Child elements</span></span>  | <span data-ttu-id="19179-115">**entry**, **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="19179-115">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="19179-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19179-116">Remarks</span></span>

<span data-ttu-id="19179-117">Este elemento define el número de veces que Windows Media Player repite, o recorre en bucle, los clips definidos por los elementos **entry** y **ENTRYREF** dentro del ámbito de este elemento.</span><span class="sxs-lookup"><span data-stu-id="19179-117">This element defines the number of times Windows Media Player repeats, or loops through, the clips defined by the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span> <span data-ttu-id="19179-118">Solo es válido el primer elemento **REPEAT** de un metarchivo; los elementos de **repetición** subsiguientes se omiten.</span><span class="sxs-lookup"><span data-stu-id="19179-118">Only the first **REPEAT** element in a metafile is valid; subsequent **REPEAT** elements are ignored.</span></span>

<span data-ttu-id="19179-119">Si no se define ningún atributo de **recuento** , el contenido de los elementos de **entrada** y **ENTRYREF** asociados se repite un número infinito de veces.</span><span class="sxs-lookup"><span data-stu-id="19179-119">If no **COUNT** attribute is defined, the content in the associated **ENTRY** and **ENTRYREF** elements repeats an infinite number of times.</span></span> <span data-ttu-id="19179-120">Un valor de cero hace que Windows Media Player omita el elemento **REPEAT** y reproduzca el contenido una vez.</span><span class="sxs-lookup"><span data-stu-id="19179-120">A value of zero causes Windows Media Player to ignore the **REPEAT** element and play the content once.</span></span>

## <a name="examples"></a><span data-ttu-id="19179-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="19179-121">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="19179-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19179-122">Requirements</span></span>



| <span data-ttu-id="19179-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="19179-123">Requirement</span></span> | <span data-ttu-id="19179-124">Value</span><span class="sxs-lookup"><span data-stu-id="19179-124">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="19179-125">Versión</span><span class="sxs-lookup"><span data-stu-id="19179-125">Version</span></span><br/> | <span data-ttu-id="19179-126">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="19179-126">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19179-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="19179-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19179-128">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="19179-128">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="19179-129">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="19179-129">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





