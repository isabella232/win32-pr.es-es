---
title: IWMPDVD titleMenu, método
description: El método titleMenu detiene la reproducción y muestra el menú de título.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- método titleMenu de Windows Media Player
- método titleMenu Windows Media Player, interfaz IWMPDVD
- Interfaz IWMPDVD Windows Media Player, método titleMenu
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0889a3f65ccefe4e09bb5ff47a66867681dcc801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661219"
---
# <a name="iwmpdvdtitlemenu-method"></a><span data-ttu-id="46742-106">IWMPDVD:: titleMenu (método)</span><span class="sxs-lookup"><span data-stu-id="46742-106">IWMPDVD::titleMenu method</span></span>

<span data-ttu-id="46742-107">El método **titleMenu** detiene la reproducción y muestra el menú de título.</span><span class="sxs-lookup"><span data-stu-id="46742-107">The **titleMenu** method stops playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="46742-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46742-108">Syntax</span></span>


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a><span data-ttu-id="46742-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46742-109">Parameters</span></span>

<span data-ttu-id="46742-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="46742-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46742-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46742-111">Return value</span></span>

<span data-ttu-id="46742-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="46742-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46742-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46742-113">Remarks</span></span>

<span data-ttu-id="46742-114">Cada DVD se crea de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="46742-114">Every DVD is authored differently.</span></span> <span data-ttu-id="46742-115">El DVD debe contener un menú para que este método funcione.</span><span class="sxs-lookup"><span data-stu-id="46742-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="46742-116">Algunos DVDs se crean para que los métodos **IWMPDVD.** **titleMenu y** abran el mismo menú.</span><span class="sxs-lookup"><span data-stu-id="46742-116">Some DVDs are authored so that the **IWMPDVD.topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="46742-117">El método **titleMenu** normalmente invoca el menú de título, pero puede invocar el menú superior si no hay ningún menú de título disponible.</span><span class="sxs-lookup"><span data-stu-id="46742-117">The **titleMenu** method usually invokes the title menu, but it may invoke the top menu if there is no title menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="46742-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46742-118">Requirements</span></span>



| <span data-ttu-id="46742-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="46742-119">Requirement</span></span> | <span data-ttu-id="46742-120">Value</span><span class="sxs-lookup"><span data-stu-id="46742-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46742-121">Versión</span><span class="sxs-lookup"><span data-stu-id="46742-121">Version</span></span><br/>   | <span data-ttu-id="46742-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="46742-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="46742-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="46742-123">Namespace</span></span><br/> | <span data-ttu-id="46742-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="46742-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="46742-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="46742-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="46742-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="46742-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46742-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="46742-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46742-128">**Interfaz IWMPDVD (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="46742-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="46742-129">**IWMPDVD. webmenu (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="46742-129">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





