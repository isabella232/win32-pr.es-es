---
title: Interfaz IDWriteColorGlyphRunEnumerator
description: Esta interfaz permite a la aplicación enumerar a través de las ejecuciones del glifo de color.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Interfaz IDWriteColorGlyphRunEnumerator de escritura directa
- IDWriteColorGlyphRunEnumerator interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802828"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a><span data-ttu-id="411a0-105">Interfaz IDWriteColorGlyphRunEnumerator</span><span class="sxs-lookup"><span data-stu-id="411a0-105">IDWriteColorGlyphRunEnumerator interface</span></span>

<span data-ttu-id="411a0-106">Esta interfaz permite a la aplicación enumerar a través de las ejecuciones del glifo de color.</span><span class="sxs-lookup"><span data-stu-id="411a0-106">This interface allows the application to enumerate through the color glyph runs.</span></span> <span data-ttu-id="411a0-107">El enumerador enumera las capas de una de vuelta al orden Front para la disposición en capas adecuada.</span><span class="sxs-lookup"><span data-stu-id="411a0-107">The enumerator enumerates the layers in a back to front order for appropriate layering.</span></span>

## <a name="members"></a><span data-ttu-id="411a0-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="411a0-108">Members</span></span>

<span data-ttu-id="411a0-109">La interfaz **IDWriteColorGlyphRunEnumerator** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="411a0-109">The **IDWriteColorGlyphRunEnumerator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="411a0-110">**IDWriteColorGlyphRunEnumerator** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="411a0-110">**IDWriteColorGlyphRunEnumerator** also has these types of members:</span></span>

-   [<span data-ttu-id="411a0-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="411a0-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="411a0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="411a0-112">Methods</span></span>

<span data-ttu-id="411a0-113">La interfaz **IDWriteColorGlyphRunEnumerator** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="411a0-113">The **IDWriteColorGlyphRunEnumerator** interface has these methods.</span></span>



| <span data-ttu-id="411a0-114">Método</span><span class="sxs-lookup"><span data-stu-id="411a0-114">Method</span></span>                                                                | <span data-ttu-id="411a0-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="411a0-115">Description</span></span>                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="411a0-116">**GetCurrentRun**</span><span class="sxs-lookup"><span data-stu-id="411a0-116">**GetCurrentRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | <span data-ttu-id="411a0-117">Devuelve la ejecución del glifo actual del enumerador.</span><span class="sxs-lookup"><span data-stu-id="411a0-117">Returns the current glyph run of the enumerator.</span></span><br/> |
| [<span data-ttu-id="411a0-118">**MoveNext**</span><span class="sxs-lookup"><span data-stu-id="411a0-118">**MoveNext**</span></span>](idwritecolorglyphrunenumerator-movenext.md)           | <span data-ttu-id="411a0-119">Desplácese a la siguiente ejecución del glifo en el enumerador.</span><span class="sxs-lookup"><span data-stu-id="411a0-119">Move to the next glyph run in the enumerator.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="411a0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="411a0-120">Requirements</span></span>



| <span data-ttu-id="411a0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="411a0-121">Requirement</span></span> | <span data-ttu-id="411a0-122">Value</span><span class="sxs-lookup"><span data-stu-id="411a0-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="411a0-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="411a0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="411a0-124">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="411a0-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="411a0-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="411a0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="411a0-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="411a0-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="411a0-127">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="411a0-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="411a0-128">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="411a0-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="411a0-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="411a0-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="411a0-130"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="411a0-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="411a0-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="411a0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="411a0-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="411a0-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

