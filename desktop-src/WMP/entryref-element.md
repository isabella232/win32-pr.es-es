---
title: Elemento ENTRYREF
description: El elemento ENTRYREF apunta a los elementos de entrada de un metarchivo externo.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Elemento ENTRYREF Media Player Windows
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698719"
---
# <a name="entryref-element"></a><span data-ttu-id="40d9c-104">Elemento ENTRYREF</span><span class="sxs-lookup"><span data-stu-id="40d9c-104">ENTRYREF Element</span></span>

<span data-ttu-id="40d9c-105">El elemento **ENTRYREF** apunta a los elementos de **entrada** de un metarchivo externo.</span><span class="sxs-lookup"><span data-stu-id="40d9c-105">The **ENTRYREF** element points to the **ENTRY** elements in an external metafile.</span></span>

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="40d9c-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="40d9c-106">Attributes</span></span>

<span data-ttu-id="40d9c-107">**Href** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="40d9c-107">**HREF** (required)</span></span>

<span data-ttu-id="40d9c-108">Dirección URL de un metarchivo al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="40d9c-108">URL to a referenced metafile.</span></span>

<span data-ttu-id="40d9c-109">**CLIENTBIND**</span><span class="sxs-lookup"><span data-stu-id="40d9c-109">**CLIENTBIND**</span></span>

<span data-ttu-id="40d9c-110">Este atributo ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="40d9c-110">This attribute is no longer supported.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="40d9c-111">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="40d9c-111">Parent/Child Elements</span></span>



| <span data-ttu-id="40d9c-112">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="40d9c-112">Hierarchy</span></span>       | <span data-ttu-id="40d9c-113">Elementos</span><span class="sxs-lookup"><span data-stu-id="40d9c-113">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="40d9c-114">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="40d9c-114">Parent elements</span></span> | <span data-ttu-id="40d9c-115">**ASX**, **evento**, **repetición**</span><span class="sxs-lookup"><span data-stu-id="40d9c-115">**ASX**, **EVENT**, **REPEAT**</span></span> |
| <span data-ttu-id="40d9c-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="40d9c-116">Child elements</span></span>  | <span data-ttu-id="40d9c-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="40d9c-117">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="40d9c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40d9c-118">Remarks</span></span>

<span data-ttu-id="40d9c-119">Este elemento apunta al contenido de un metarchivo externo.</span><span class="sxs-lookup"><span data-stu-id="40d9c-119">This element points to the contents of an external metafile.</span></span> <span data-ttu-id="40d9c-120">Windows Media Player procesa los elementos de **entrada** del metarchivo al que se hace referencia como si estuvieran incluidos en el metarchivo principal situado en la posición del elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="40d9c-120">Windows Media Player processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="40d9c-121">Sin embargo, omite cualquier elemento de **entrada** del metarchivo al que se hace referencia que tenga el atributo **SKIPIFREF** establecido en sí.</span><span class="sxs-lookup"><span data-stu-id="40d9c-121">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="40d9c-122">Windows Media Player 7,0, 7,1 y Windows Media Player para Windows XP omiten los elementos **ENTRYREF** del metarchivo al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="40d9c-122">Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="40d9c-123">Por lo tanto, los metaarchivos solo se pueden anidar un nivel en profundidad al usar estas versiones del reproductor.</span><span class="sxs-lookup"><span data-stu-id="40d9c-123">Thus, metafiles can only be nested one level deep when using these versions of the Player.</span></span> <span data-ttu-id="40d9c-124">Windows Media Player también omite el elemento **ASX** en el archivo al que se hace referencia junto con sus atributos.</span><span class="sxs-lookup"><span data-stu-id="40d9c-124">Windows Media Player also ignores the **ASX** element in the referenced file along with its attributes.</span></span> <span data-ttu-id="40d9c-125">Windows Media Player 9 series o posterior admiten el anidamiento de metaarchivos hasta cinco niveles de profundidad.</span><span class="sxs-lookup"><span data-stu-id="40d9c-125">Windows Media Player 9 Series or later supports nesting metafiles up to five levels deep.</span></span>

<span data-ttu-id="40d9c-126">La dirección URL especificada en el atributo **href** se convierte en la dirección URL base de las direcciones URL relativas del metarchivo externo.</span><span class="sxs-lookup"><span data-stu-id="40d9c-126">The URL specified in the **HREF** attribute becomes the base URL for any relative URLs in the external metafile.</span></span> <span data-ttu-id="40d9c-127">Esta dirección URL se usa cuando se está reproduciendo una entrada del metarchivo externo y el usuario la agrega a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="40d9c-127">This URL is used when an entry from the external metafile is playing and the user adds it to the library.</span></span>

## <a name="examples"></a><span data-ttu-id="40d9c-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="40d9c-128">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="40d9c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40d9c-129">Requirements</span></span>



| <span data-ttu-id="40d9c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="40d9c-130">Requirement</span></span> | <span data-ttu-id="40d9c-131">Value</span><span class="sxs-lookup"><span data-stu-id="40d9c-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="40d9c-132">Versión</span><span class="sxs-lookup"><span data-stu-id="40d9c-132">Version</span></span><br/> | <span data-ttu-id="40d9c-133">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="40d9c-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40d9c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="40d9c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d9c-135">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="40d9c-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="40d9c-136">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="40d9c-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





