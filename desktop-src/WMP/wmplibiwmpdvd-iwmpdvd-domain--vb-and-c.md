---
title: Propiedad de dominio IWMPDVD
description: La propiedad de dominio obtiene el dominio actual del DVD.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Media Player de propiedades de dominio de Windows
- propiedad de dominio Windows Media Player, interfaz IWMPDVD
- Interfaz IWMPDVD Windows Media Player, propiedad de dominio
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653911"
---
# <a name="iwmpdvddomain-property"></a><span data-ttu-id="130e1-106">IWMPDVD::d propiedad omain</span><span class="sxs-lookup"><span data-stu-id="130e1-106">IWMPDVD::domain property</span></span>

<span data-ttu-id="130e1-107">La propiedad de **dominio** obtiene el dominio actual del DVD.</span><span class="sxs-lookup"><span data-stu-id="130e1-107">The **domain** property gets the current domain of the DVD.</span></span>

## <a name="syntax"></a><span data-ttu-id="130e1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="130e1-108">Syntax</span></span>


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a><span data-ttu-id="130e1-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="130e1-109">Property value</span></span>

<span data-ttu-id="130e1-110">**System. String** que es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="130e1-110">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="130e1-111">Value</span><span class="sxs-lookup"><span data-stu-id="130e1-111">Value</span></span>                                                                                        | <span data-ttu-id="130e1-112">Significado</span><span class="sxs-lookup"><span data-stu-id="130e1-112">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="130e1-113"><dt>firstPlay</dt></span><span class="sxs-lookup"><span data-stu-id="130e1-113"><dt>firstPlay</dt></span></span> </dl>         | <span data-ttu-id="130e1-114">Realizar la inicialización predeterminada de un disco DVD.</span><span class="sxs-lookup"><span data-stu-id="130e1-114">Performing default initialization of a DVD disc.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="130e1-115"><dt>videoManagerMenu</dt></span><span class="sxs-lookup"><span data-stu-id="130e1-115"><dt>videoManagerMenu</dt></span></span> </dl>  | <span data-ttu-id="130e1-116">Mostrar menús para todo el disco. También conocido como menú de Media Player para Windows.</span><span class="sxs-lookup"><span data-stu-id="130e1-116">Displaying menus for the entire disc. Also known as topMenu for Windows Media Player.</span></span> <span data-ttu-id="130e1-117">Normalmente denominado el menú de título o el menú superior.</span><span class="sxs-lookup"><span data-stu-id="130e1-117">Commonly called the title menu or the top menu.</span></span><br/> |
| <dl> <span data-ttu-id="130e1-118"><dt>videoTitleSetMenu</dt></span><span class="sxs-lookup"><span data-stu-id="130e1-118"><dt>videoTitleSetMenu</dt></span></span> </dl> | <span data-ttu-id="130e1-119">Mostrar los menús del conjunto de títulos actual.</span><span class="sxs-lookup"><span data-stu-id="130e1-119">Displaying menus for the current title set.</span></span> <span data-ttu-id="130e1-120">También conocido como titleMenu para Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="130e1-120">Also known as titleMenu for Windows Media Player.</span></span> <span data-ttu-id="130e1-121">Normalmente denominado menú raíz.</span><span class="sxs-lookup"><span data-stu-id="130e1-121">Commonly called the root menu.</span></span><br/>          |
| <dl> <span data-ttu-id="130e1-122"><dt>title</dt></span><span class="sxs-lookup"><span data-stu-id="130e1-122"><dt>title</dt></span></span> </dl>             | <span data-ttu-id="130e1-123">Normalmente, mostrando el título actual.</span><span class="sxs-lookup"><span data-stu-id="130e1-123">Usually, displaying the current title.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="130e1-124"><dt>stop</dt></span><span class="sxs-lookup"><span data-stu-id="130e1-124"><dt>stop</dt></span></span> </dl>              | <span data-ttu-id="130e1-125">El navegador de DVD está en el dominio de detención de DVD.</span><span class="sxs-lookup"><span data-stu-id="130e1-125">The DVD Navigator is in the DVD Stop domain.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="130e1-126"><dt>indefinido</dt></span><span class="sxs-lookup"><span data-stu-id="130e1-126"><dt>undefined</dt></span></span> </dl>         | <span data-ttu-id="130e1-127">Windows Media Player no está en ningún dominio de DVD.</span><span class="sxs-lookup"><span data-stu-id="130e1-127">Windows Media Player is not in any DVD domain.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="130e1-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="130e1-128">Remarks</span></span>

<span data-ttu-id="130e1-129">Cada DVD se crea de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="130e1-129">Every DVD is authored differently.</span></span> <span data-ttu-id="130e1-130">Algunos DVDs no contienen los dominios firstPlay, videoManagerMenu o videoTitleSetMenu.</span><span class="sxs-lookup"><span data-stu-id="130e1-130">Some DVDs do not contain the firstPlay, videoManagerMenu, or videoTitleSetMenu domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="130e1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="130e1-131">Requirements</span></span>



| <span data-ttu-id="130e1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="130e1-132">Requirement</span></span> | <span data-ttu-id="130e1-133">Value</span><span class="sxs-lookup"><span data-stu-id="130e1-133">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="130e1-134">Versión</span><span class="sxs-lookup"><span data-stu-id="130e1-134">Version</span></span><br/>   | <span data-ttu-id="130e1-135">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="130e1-135">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="130e1-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="130e1-136">Namespace</span></span><br/> | <span data-ttu-id="130e1-137">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="130e1-137">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="130e1-138">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="130e1-138">Assembly</span></span><br/>  | <dl> <span data-ttu-id="130e1-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="130e1-139"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="130e1-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="130e1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="130e1-141">**Interfaz IWMPDVD (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="130e1-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





