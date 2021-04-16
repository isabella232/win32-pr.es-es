---
title: Interfaz IDWriteTextFormat2
description: Describe las propiedades de fuente y de párrafo utilizadas para dar formato al texto y describe la información de configuración regional. | Interfaz IDWriteTextFormat2
ms.assetid: 4396d2b0-240f-ee8b-1d21-c4294fb29b51
keywords:
- Interfaz IDWriteTextFormat2 de escritura directa
- IDWriteTextFormat2 interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteTextFormat2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06abf78095953f684ed6ec3fd241c699b2b37db4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670177"
---
# <a name="idwritetextformat2-interface"></a><span data-ttu-id="15acc-106">Interfaz IDWriteTextFormat2</span><span class="sxs-lookup"><span data-stu-id="15acc-106">IDWriteTextFormat2 interface</span></span>

<span data-ttu-id="15acc-107">Describe las propiedades de fuente y de párrafo utilizadas para dar formato al texto y describe la información de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="15acc-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span>

## <a name="members"></a><span data-ttu-id="15acc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="15acc-108">Members</span></span>

<span data-ttu-id="15acc-109">La interfaz **IDWriteTextFormat2** hereda de [**IDWriteTextFormat1**](idwritetextformat1.md).</span><span class="sxs-lookup"><span data-stu-id="15acc-109">The **IDWriteTextFormat2** interface inherits from [**IDWriteTextFormat1**](idwritetextformat1.md).</span></span> <span data-ttu-id="15acc-110">**IDWriteTextFormat2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="15acc-110">**IDWriteTextFormat2** also has these types of members:</span></span>

-   [<span data-ttu-id="15acc-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="15acc-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="15acc-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="15acc-112">Methods</span></span>

<span data-ttu-id="15acc-113">La interfaz **IDWriteTextFormat2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="15acc-113">The **IDWriteTextFormat2** interface has these methods.</span></span>



| <span data-ttu-id="15acc-114">Método</span><span class="sxs-lookup"><span data-stu-id="15acc-114">Method</span></span>                                                      | <span data-ttu-id="15acc-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="15acc-115">Description</span></span>                                                                      |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="15acc-116">**GetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="15acc-116">**GetLineSpacing**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextformat2-getlinespacing) | <span data-ttu-id="15acc-117">Obtiene el conjunto de ajuste de espaciado de línea para un párrafo de texto de varias líneas.</span><span class="sxs-lookup"><span data-stu-id="15acc-117">Gets the line spacing adjustment set for a multiline text paragraph.</span></span> <br/> |
| [<span data-ttu-id="15acc-118">**SetLineSpacing**</span><span class="sxs-lookup"><span data-stu-id="15acc-118">**SetLineSpacing**</span></span>](idwritetextformat2-setlinespacing.md) | <span data-ttu-id="15acc-119">Establezca el interlineado.</span><span class="sxs-lookup"><span data-stu-id="15acc-119">Set line spacing.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="15acc-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15acc-120">Requirements</span></span>



| <span data-ttu-id="15acc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="15acc-121">Requirement</span></span> | <span data-ttu-id="15acc-122">Value</span><span class="sxs-lookup"><span data-stu-id="15acc-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15acc-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15acc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="15acc-124">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="15acc-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="15acc-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15acc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="15acc-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="15acc-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="15acc-127">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15acc-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="15acc-128">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="15acc-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="15acc-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15acc-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="15acc-130"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15acc-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="15acc-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15acc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15acc-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15acc-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15acc-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="15acc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15acc-134">**IDWriteTextFormat1**</span><span class="sxs-lookup"><span data-stu-id="15acc-134">**IDWriteTextFormat1**</span></span>](idwritetextformat1.md)
</dt> </dl>

 

