---
title: Elemento SMIL
description: El elemento SMIL siempre es el elemento de nivel superior de un archivo de lista de reproducción de Windows Media (WPL). Especifica que el archivo usa la gramática y la sintaxis de SMIL (lenguaje de integración multimedia sincronizado).
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Media Player de ventanas de elemento SMIL
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661121"
---
# <a name="smil-element"></a><span data-ttu-id="86d0f-105">Elemento SMIL</span><span class="sxs-lookup"><span data-stu-id="86d0f-105">smil Element</span></span>

<span data-ttu-id="86d0f-106">El elemento **SMIL** siempre es el elemento de nivel superior de un archivo de lista de reproducción de Windows Media (Wpl).</span><span class="sxs-lookup"><span data-stu-id="86d0f-106">The **smil** element is always the top level element in a Windows Media Playlist (WPL) file.</span></span> <span data-ttu-id="86d0f-107">Especifica que el archivo usa la gramática y la sintaxis de SMIL (lenguaje de integración multimedia sincronizado).</span><span class="sxs-lookup"><span data-stu-id="86d0f-107">It specifies that the file uses SMIL (Synchronized Multimedia Integration Language) syntax and grammar.</span></span>

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a><span data-ttu-id="86d0f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="86d0f-108">Attributes</span></span>

<span data-ttu-id="86d0f-109">Este elemento no tiene atributos.</span><span class="sxs-lookup"><span data-stu-id="86d0f-109">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="86d0f-110">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="86d0f-110">Parent/Child Elements</span></span>



| <span data-ttu-id="86d0f-111">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="86d0f-111">Hierarchy</span></span> | <span data-ttu-id="86d0f-112">Elementos</span><span class="sxs-lookup"><span data-stu-id="86d0f-112">Elements</span></span>                                           |
|-----------|----------------------------------------------------|
| <span data-ttu-id="86d0f-113">Parent</span><span class="sxs-lookup"><span data-stu-id="86d0f-113">Parent</span></span>    | <span data-ttu-id="86d0f-114">None</span><span class="sxs-lookup"><span data-stu-id="86d0f-114">None</span></span>                                               |
| <span data-ttu-id="86d0f-115">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="86d0f-115">Child</span></span>     | <span data-ttu-id="86d0f-116">[encabezado](head-element.md), [cuerpo](body-element.md)</span><span class="sxs-lookup"><span data-stu-id="86d0f-116">[head](head-element.md), [body](body-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="86d0f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86d0f-117">Remarks</span></span>

<span data-ttu-id="86d0f-118">Cada lista de reproducción de Windows Media debe tener el elemento **SMIL** en su raíz.</span><span class="sxs-lookup"><span data-stu-id="86d0f-118">Every Windows Media Playlist must have the **smil** element at its root.</span></span>

## <a name="examples"></a><span data-ttu-id="86d0f-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="86d0f-119">Examples</span></span>


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a><span data-ttu-id="86d0f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86d0f-120">Requirements</span></span>



| <span data-ttu-id="86d0f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="86d0f-121">Requirement</span></span> | <span data-ttu-id="86d0f-122">Value</span><span class="sxs-lookup"><span data-stu-id="86d0f-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="86d0f-123">Versión</span><span class="sxs-lookup"><span data-stu-id="86d0f-123">Version</span></span><br/> | <span data-ttu-id="86d0f-124">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="86d0f-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86d0f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="86d0f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86d0f-126">**Elemento BODY**</span><span class="sxs-lookup"><span data-stu-id="86d0f-126">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="86d0f-127">**Elemento de encabezado**</span><span class="sxs-lookup"><span data-stu-id="86d0f-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="86d0f-128">**Referencia de elementos de lista de reproducción de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="86d0f-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





