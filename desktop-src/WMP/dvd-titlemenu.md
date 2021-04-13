---
title: DVD. titleMenu (método)
description: El método titleMenu detiene la reproducción del título y muestra el menú de título.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- método titleMenu de Windows Media Player
- método titleMenu de Windows Media Player, clase de DVD
- Clase de DVD Windows Media Player, método titleMenu
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359716"
---
# <a name="dvdtitlemenu-method"></a><span data-ttu-id="48c7c-106">DVD. titleMenu (método)</span><span class="sxs-lookup"><span data-stu-id="48c7c-106">DVD.titleMenu method</span></span>

<span data-ttu-id="48c7c-107">El método **titleMenu** detiene la reproducción del título y muestra el menú de título.</span><span class="sxs-lookup"><span data-stu-id="48c7c-107">The **titleMenu** method stops title playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="48c7c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48c7c-108">Syntax</span></span>


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a><span data-ttu-id="48c7c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48c7c-109">Parameters</span></span>

<span data-ttu-id="48c7c-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="48c7c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="48c7c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48c7c-111">Return value</span></span>

<span data-ttu-id="48c7c-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="48c7c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48c7c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48c7c-113">Remarks</span></span>

<span data-ttu-id="48c7c-114">Cada DVD se crea de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="48c7c-114">Every DVD is authored differently.</span></span> <span data-ttu-id="48c7c-115">El DVD debe contener un menú para que este método funcione.</span><span class="sxs-lookup"><span data-stu-id="48c7c-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="48c7c-116">Algunos DVDs se crean para que los métodos de **menú** y **titleMenu** abran el mismo menú.</span><span class="sxs-lookup"><span data-stu-id="48c7c-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="48c7c-117">El método **titleMenu** normalmente invoca el menú de título, pero puede invocar el menú superior en su lugar, si no hay ningún menú de título disponible.</span><span class="sxs-lookup"><span data-stu-id="48c7c-117">The **titleMenu** method usually invokes the title menu but it may invoke the top menu instead, if there is no title menu available.</span></span>

<span data-ttu-id="48c7c-118">**Windows Media Player 10 Mobile:** Este método siempre se realiza correctamente, pero no realiza la operación deseada.</span><span class="sxs-lookup"><span data-stu-id="48c7c-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="48c7c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48c7c-119">Requirements</span></span>



| <span data-ttu-id="48c7c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="48c7c-120">Requirement</span></span> | <span data-ttu-id="48c7c-121">Value</span><span class="sxs-lookup"><span data-stu-id="48c7c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="48c7c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48c7c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="48c7c-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="48c7c-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48c7c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48c7c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="48c7c-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="48c7c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="48c7c-126">Versión</span><span class="sxs-lookup"><span data-stu-id="48c7c-126">Version</span></span><br/>                  | <span data-ttu-id="48c7c-127">Windows Media Player para Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="48c7c-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="48c7c-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48c7c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48c7c-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48c7c-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48c7c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="48c7c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c7c-131">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="48c7c-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="48c7c-132">**DVD. Menu**</span><span class="sxs-lookup"><span data-stu-id="48c7c-132">**DVD.topMenu**</span></span>](dvd-topmenu.md)
</dt> </dl>

 

 





