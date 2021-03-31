---
title: DVD. webmenu (método)
description: El método de menú de menús detiene la reproducción del título y muestra el menú superior (o raíz) del título actual.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- método de menú de menús Media Player Windows
- método de menú de menús Windows Media Player, clase de DVD
- Clase de DVD Windows Media Player, método de menú de menús
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491272"
---
# <a name="dvdtopmenu-method"></a><span data-ttu-id="c7c5a-106">DVD. webmenu (método)</span><span class="sxs-lookup"><span data-stu-id="c7c5a-106">DVD.topMenu method</span></span>

<span data-ttu-id="c7c5a-107">El método de **menú de menús** detiene la reproducción del título y muestra el menú superior (o raíz) del título actual.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-107">The **topMenu** method stops title playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c5a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7c5a-108">Syntax</span></span>


```JScript
DVD.topMenu()
```



## <a name="parameters"></a><span data-ttu-id="c7c5a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7c5a-109">Parameters</span></span>

<span data-ttu-id="c7c5a-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7c5a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7c5a-111">Return value</span></span>

<span data-ttu-id="c7c5a-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c5a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7c5a-113">Remarks</span></span>

<span data-ttu-id="c7c5a-114">Cada DVD se crea de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-114">Every DVD is authored differently.</span></span> <span data-ttu-id="c7c5a-115">El DVD debe contener un menú para que este método funcione.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="c7c5a-116">Algunos DVDs se crean para que los métodos de **menú** y **titleMenu** abran el mismo menú.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="c7c5a-117">El método de **menú de menús** normalmente invoca el menú superior (o raíz), pero puede invocar el menú de título en su lugar, si no hay ningún menú raíz disponible.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-117">The **topMenu** method usually invokes the top (or root) menu but it may invoke the title menu instead, if there is no root menu available.</span></span>

<span data-ttu-id="c7c5a-118">**Windows Media Player 10 Mobile:** Este método siempre se realiza correctamente, pero no realiza la operación deseada.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c5a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7c5a-119">Requirements</span></span>



| <span data-ttu-id="c7c5a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7c5a-120">Requirement</span></span> | <span data-ttu-id="c7c5a-121">Value</span><span class="sxs-lookup"><span data-stu-id="c7c5a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c5a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7c5a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c5a-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c7c5a-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7c5a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7c5a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c5a-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7c5a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c7c5a-126">Versión</span><span class="sxs-lookup"><span data-stu-id="c7c5a-126">Version</span></span><br/>                  | <span data-ttu-id="c7c5a-127">Windows Media Player para Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="c7c5a-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="c7c5a-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7c5a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7c5a-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7c5a-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7c5a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7c5a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c5a-131">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="c7c5a-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="c7c5a-132">**DVD. titleMenu**</span><span class="sxs-lookup"><span data-stu-id="c7c5a-132">**DVD.titleMenu**</span></span>](dvd-titlemenu.md)
</dt> </dl>

 

 





