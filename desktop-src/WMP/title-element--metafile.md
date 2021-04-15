---
title: TITLE (elemento) (metarchivo)
description: El elemento TITLE define una cadena de texto que especifica el título de un elemento ASX o ENTRY.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Elemento TITLE (metarchivo) Windows Media Player
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709082"
---
# <a name="title-element-metafile"></a><span data-ttu-id="7431a-104">TITLE (elemento) (metarchivo)</span><span class="sxs-lookup"><span data-stu-id="7431a-104">TITLE Element (metafile)</span></span>

<span data-ttu-id="7431a-105">El elemento **title** define una cadena de texto que especifica el título de un elemento **ASX** o **entry** .</span><span class="sxs-lookup"><span data-stu-id="7431a-105">The **TITLE** element defines a text string specifying the title for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a><span data-ttu-id="7431a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="7431a-106">Attributes</span></span>

<span data-ttu-id="7431a-107">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="7431a-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="7431a-108">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="7431a-108">Parent/Child Elements</span></span>



| <span data-ttu-id="7431a-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="7431a-109">Hierarchy</span></span>       | <span data-ttu-id="7431a-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="7431a-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="7431a-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="7431a-111">Parent elements</span></span> | <span data-ttu-id="7431a-112">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="7431a-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="7431a-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7431a-113">Child elements</span></span>  | <span data-ttu-id="7431a-114">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7431a-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="7431a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7431a-115">Remarks</span></span>

<span data-ttu-id="7431a-116">Este elemento define una cadena de texto que especifica el título de un elemento **ASX** o **entry** .</span><span class="sxs-lookup"><span data-stu-id="7431a-116">This element defines a text string that specifies the title of an **ASX** or **ENTRY** element.</span></span> <span data-ttu-id="7431a-117">El título se muestra en el panel de información y en el cuadro de diálogo **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="7431a-117">The title is displayed in the display panel and **Properties** dialog box.</span></span>

<span data-ttu-id="7431a-118">Cuando este elemento aparece dentro de un elemento **ASX** , el texto se muestra como **Mostrar** información.</span><span class="sxs-lookup"><span data-stu-id="7431a-118">When this element appears within an **ASX** element, the text is displayed as **Show** information.</span></span> <span data-ttu-id="7431a-119">Cuando este elemento aparece dentro de un elemento de **entrada** , el texto se muestra como información de **recorte** .</span><span class="sxs-lookup"><span data-stu-id="7431a-119">When this element appears within an **ENTRY** element, the text is displayed as **Clip** information.</span></span>

<span data-ttu-id="7431a-120">Si un elemento **MOREINFO** también se usa con el elemento (primario) asociado, es el texto del título en el que el usuario hace clic para obtener acceso a la dirección URL definida en el elemento **MOREINFO** .</span><span class="sxs-lookup"><span data-stu-id="7431a-120">If a **MOREINFO** element is also used with the associated (parent) element, it is the title text that the user clicks to access the URL defined in the **MOREINFO** element.</span></span>

<span data-ttu-id="7431a-121">Cada elemento **ASX** y **entry** primarios debe contener como máximo un elemento secundario **title** .</span><span class="sxs-lookup"><span data-stu-id="7431a-121">Each parent **ASX** and **ENTRY** element should contain at most one child **TITLE** element.</span></span> <span data-ttu-id="7431a-122">Varios elementos **title** después del primero se omitirán y no se mostrarán.</span><span class="sxs-lookup"><span data-stu-id="7431a-122">Multiple **TITLE** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="7431a-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7431a-123">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="7431a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7431a-124">Requirements</span></span>



| <span data-ttu-id="7431a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7431a-125">Requirement</span></span> | <span data-ttu-id="7431a-126">Value</span><span class="sxs-lookup"><span data-stu-id="7431a-126">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="7431a-127">Versión</span><span class="sxs-lookup"><span data-stu-id="7431a-127">Version</span></span><br/> | <span data-ttu-id="7431a-128">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="7431a-128">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7431a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7431a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7431a-130">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7431a-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="7431a-131">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="7431a-131">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





