---
title: Elemento COPYRIGHT (msfeeds. h)
description: El elemento COPYRIGHT define una cadena de texto que especifica la información de copyright de un elemento ASX o ENTRY.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Elemento COPYRIGHT de Windows Media Player
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699926"
---
# <a name="copyright-element"></a><span data-ttu-id="1bfae-104">Elemento COPYRIGHT</span><span class="sxs-lookup"><span data-stu-id="1bfae-104">COPYRIGHT Element</span></span>

<span data-ttu-id="1bfae-105">El elemento **Copyright** define una cadena de texto que especifica la información de copyright de un elemento **ASX** o **entry** .</span><span class="sxs-lookup"><span data-stu-id="1bfae-105">The **COPYRIGHT** element defines a text string specifying the copyright information for an **ASX** or **ENTRY** element.</span></span>

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a><span data-ttu-id="1bfae-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="1bfae-106">Attributes</span></span>

<span data-ttu-id="1bfae-107">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="1bfae-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="1bfae-108">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="1bfae-108">Parent/Child Elements</span></span>



| <span data-ttu-id="1bfae-109">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="1bfae-109">Hierarchy</span></span>       | <span data-ttu-id="1bfae-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="1bfae-110">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="1bfae-111">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1bfae-111">Parent elements</span></span> | <span data-ttu-id="1bfae-112">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="1bfae-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="1bfae-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1bfae-113">Child elements</span></span>  | <span data-ttu-id="1bfae-114">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1bfae-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="1bfae-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1bfae-115">Remarks</span></span>

<span data-ttu-id="1bfae-116">Este elemento define una cadena de texto que especifica la información de copyright para un elemento **ASX** o **entry** .</span><span class="sxs-lookup"><span data-stu-id="1bfae-116">This element defines a text string that specifies the copyright information for an **ASX** or **ENTRY** element.</span></span>

<span data-ttu-id="1bfae-117">Cuando este elemento aparece dentro de un elemento **ASX** , la cadena de copyright solo se muestra como **Mostrar** información.</span><span class="sxs-lookup"><span data-stu-id="1bfae-117">When this element appears within an **ASX** element, the copyright string is displayed only as **Show** information.</span></span> <span data-ttu-id="1bfae-118">Cuando este elemento aparece dentro de un elemento de **entrada** , el texto se muestra como información de recorte.</span><span class="sxs-lookup"><span data-stu-id="1bfae-118">When this element appears within an **ENTRY** element, the text is displayed as clip information.</span></span> <span data-ttu-id="1bfae-119">Cada elemento **ASX** y **entry** primarios debe contener como máximo un elemento secundario de **Copyright** .</span><span class="sxs-lookup"><span data-stu-id="1bfae-119">Each parent **ASX** and **ENTRY** element should contain at most one child **COPYRIGHT** element.</span></span> <span data-ttu-id="1bfae-120">Varios elementos de **Copyright** después del primero se omitirán y no se mostrarán.</span><span class="sxs-lookup"><span data-stu-id="1bfae-120">Multiple **COPYRIGHT** elements after the first will be ignored and will not be displayed.</span></span>

<span data-ttu-id="1bfae-121">Es posible que los caracteres de los símbolos de copyright y de registro de marcas comerciales (o) no se muestren correctamente si el metarchivo no se codifica con el esquema de codificación UTF-8.</span><span class="sxs-lookup"><span data-stu-id="1bfae-121">The characters for copyright and trademark registration symbols (   or   ) may not display properly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="1bfae-122">En este caso, para mostrar correctamente cualquiera de estos símbolos para todos los usuarios, puede usar en su lugar los equivalentes ASCII (c) y (R).</span><span class="sxs-lookup"><span data-stu-id="1bfae-122">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (R) instead.</span></span>

<span data-ttu-id="1bfae-123">Si el metarchivo está codificado con UTF-8, los símbolos de copyright y marca comercial se mostrarán correctamente.</span><span class="sxs-lookup"><span data-stu-id="1bfae-123">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="1bfae-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1bfae-124">Examples</span></span>


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a><span data-ttu-id="1bfae-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bfae-125">Requirements</span></span>



| <span data-ttu-id="1bfae-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bfae-126">Requirement</span></span> | <span data-ttu-id="1bfae-127">Value</span><span class="sxs-lookup"><span data-stu-id="1bfae-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfae-128">Versión</span><span class="sxs-lookup"><span data-stu-id="1bfae-128">Version</span></span><br/> | <span data-ttu-id="1bfae-129">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="1bfae-129">Windows Media Player version 7.0 or later</span></span><br/>                                 |
| <span data-ttu-id="1bfae-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1bfae-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1bfae-131"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bfae-131"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bfae-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1bfae-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bfae-133">**Agregar caracteres de copyright a los metaarchivos**</span><span class="sxs-lookup"><span data-stu-id="1bfae-133">**Adding Copyright Characters to Metafiles**</span></span>](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[<span data-ttu-id="1bfae-134">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1bfae-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="1bfae-135">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="1bfae-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





