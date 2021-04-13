---
title: DVD. dominio
description: La propiedad de dominio recupera el dominio actual del DVD.
ms.assetid: 74f4a6a3-8518-48c7-b023-f0255a3a62fd
keywords:
- DVD. dominio Windows Media Player
topic_type:
- apiref
api_name:
- DVD.domain
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4a2af92abe533fed7a13e48cb7c0724223bbc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359717"
---
# <a name="dvddomain"></a><span data-ttu-id="e7bc5-104">DVD. dominio</span><span class="sxs-lookup"><span data-stu-id="e7bc5-104">DVD.domain</span></span>

<span data-ttu-id="e7bc5-105">La propiedad de **dominio** recupera el dominio actual del DVD.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-105">The **domain** property retrieves the current domain of the DVD.</span></span>

``` syntax
player.dvd.domain
      
```

## <a name="possible-values"></a><span data-ttu-id="e7bc5-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="e7bc5-106">Possible Values</span></span>

<span data-ttu-id="e7bc5-107">Esta propiedad es una **cadena** de solo lectura que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-107">This property is a read-only **String** containing one of the following values.</span></span>



| <span data-ttu-id="e7bc5-108">String</span><span class="sxs-lookup"><span data-stu-id="e7bc5-108">String</span></span>            | <span data-ttu-id="e7bc5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7bc5-109">Description</span></span>                                                                                                                           |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7bc5-110">firstPlay</span><span class="sxs-lookup"><span data-stu-id="e7bc5-110">firstPlay</span></span>         | <span data-ttu-id="e7bc5-111">Realizar la inicialización predeterminada de un disco DVD.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-111">Performing default initialization of a DVD disc.</span></span>                                                                                      |
| <span data-ttu-id="e7bc5-112">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="e7bc5-112">videoManagerMenu</span></span>  | <span data-ttu-id="e7bc5-113">Mostrar menús para todo el disco. También conocido como menú de Media Player para Windows.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-113">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="e7bc5-114">Normalmente denominado el menú de título o el menú superior.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-114">Commonly called the title menu or the top menu.</span></span> |
| <span data-ttu-id="e7bc5-115">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="e7bc5-115">videoTitleSetMenu</span></span> | <span data-ttu-id="e7bc5-116">Mostrar menús para el conjunto de títulos actual.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-116">Displaying menus for current title set.</span></span> <span data-ttu-id="e7bc5-117">También conocido como titleMenu para Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-117">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="e7bc5-118">Normalmente denominado menú raíz.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-118">Commonly called the root menu.</span></span>              |
| <span data-ttu-id="e7bc5-119">title</span><span class="sxs-lookup"><span data-stu-id="e7bc5-119">title</span></span>             | <span data-ttu-id="e7bc5-120">Normalmente, mostrando el título actual.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-120">Usually displaying the current title.</span></span>                                                                                                 |
| <span data-ttu-id="e7bc5-121">stop</span><span class="sxs-lookup"><span data-stu-id="e7bc5-121">stop</span></span>              | <span data-ttu-id="e7bc5-122">El navegador de DVD está en el dominio de detención de DVD.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-122">The DVD Navigator is in the DVD Stop domain.</span></span>                                                                                          |
| <span data-ttu-id="e7bc5-123">no definido</span><span class="sxs-lookup"><span data-stu-id="e7bc5-123">undefined</span></span>         | <span data-ttu-id="e7bc5-124">El reproductor no está en ningún dominio de DVD.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-124">Player is not in any DVD domain.</span></span>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="e7bc5-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7bc5-125">Remarks</span></span>

<span data-ttu-id="e7bc5-126">Cada DVD se crea de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-126">Every DVD is authored differently.</span></span> <span data-ttu-id="e7bc5-127">Algunos DVDs no contienen los dominios firstPlay, videoManagerMenu o videoTitleSetMenu.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-127">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

<span data-ttu-id="e7bc5-128">**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="e7bc5-128">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7bc5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7bc5-129">Requirements</span></span>



| <span data-ttu-id="e7bc5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7bc5-130">Requirement</span></span> | <span data-ttu-id="e7bc5-131">Value</span><span class="sxs-lookup"><span data-stu-id="e7bc5-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7bc5-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7bc5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e7bc5-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e7bc5-133">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e7bc5-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7bc5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e7bc5-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7bc5-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e7bc5-136">Versión</span><span class="sxs-lookup"><span data-stu-id="e7bc5-136">Version</span></span><br/>                  | <span data-ttu-id="e7bc5-137">Windows Media Player para Windows XP o posterior</span><span class="sxs-lookup"><span data-stu-id="e7bc5-137">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="e7bc5-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7bc5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7bc5-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7bc5-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7bc5-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7bc5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7bc5-141">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="e7bc5-141">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





