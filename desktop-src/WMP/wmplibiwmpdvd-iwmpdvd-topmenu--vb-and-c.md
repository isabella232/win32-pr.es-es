---
title: IWMPDVD (método de menú)
description: El método de menú de menús detiene la reproducción y muestra el menú superior (o raíz) del título actual.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- método de menú de menús Media Player Windows
- método de menú de menús Windows Media Player, interfaz IWMPDVD
- Interfaz IWMPDVD Windows Media Player, método de menú de menús
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718973"
---
# <a name="iwmpdvdtopmenu-method"></a><span data-ttu-id="81e61-106">IWMPDVD:: webmenu (método)</span><span class="sxs-lookup"><span data-stu-id="81e61-106">IWMPDVD::topMenu method</span></span>

<span data-ttu-id="81e61-107">El método de **menú de menús** detiene la reproducción y muestra el menú superior (o raíz) del título actual.</span><span class="sxs-lookup"><span data-stu-id="81e61-107">The **topMenu** method stops playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e61-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81e61-108">Syntax</span></span>


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a><span data-ttu-id="81e61-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81e61-109">Parameters</span></span>

<span data-ttu-id="81e61-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="81e61-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81e61-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81e61-111">Return value</span></span>

<span data-ttu-id="81e61-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="81e61-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81e61-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81e61-113">Remarks</span></span>

<span data-ttu-id="81e61-114">Cada DVD se crea de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="81e61-114">Every DVD is authored differently.</span></span> <span data-ttu-id="81e61-115">El DVD debe contener un menú para que este método funcione.</span><span class="sxs-lookup"><span data-stu-id="81e61-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="81e61-116">Algunos DVDs se crean para que los métodos de **menú** y **IWMPDVD. titleMenu** abran el mismo menú.</span><span class="sxs-lookup"><span data-stu-id="81e61-116">Some DVDs are authored so that the **topMenu** and **IWMPDVD.titleMenu** methods open the same menu.</span></span> <span data-ttu-id="81e61-117">El método de **menú de menús** suele invocar el menú superior (o raíz), pero puede invocar el menú de título si no hay ningún menú raíz disponible.</span><span class="sxs-lookup"><span data-stu-id="81e61-117">The **topMenu** method usually invokes the top (or root) menu, but it may invoke the title menu if there is no root menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="81e61-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81e61-118">Requirements</span></span>



| <span data-ttu-id="81e61-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="81e61-119">Requirement</span></span> | <span data-ttu-id="81e61-120">Value</span><span class="sxs-lookup"><span data-stu-id="81e61-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81e61-121">Versión</span><span class="sxs-lookup"><span data-stu-id="81e61-121">Version</span></span><br/>   | <span data-ttu-id="81e61-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="81e61-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="81e61-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="81e61-123">Namespace</span></span><br/> | <span data-ttu-id="81e61-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="81e61-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="81e61-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="81e61-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="81e61-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="81e61-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81e61-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="81e61-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e61-128">**Interfaz IWMPDVD (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="81e61-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="81e61-129">**IWMPDVD. titleMenu (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="81e61-129">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





