---
title: Interfaz IWMPControls2 (VB y C, Wmp.h)
description: Proporciona un método que complementa la interfaz IWMPControls.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2 (VB y C) interfaz de Windows Media Player
- IWMPControls2 (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690424"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a><span data-ttu-id="a0091-105">Interfaz IWMPControls2 (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="a0091-105">IWMPControls2 (VB and C#) interface</span></span>

<span data-ttu-id="a0091-106">Proporciona un método que complementa la interfaz [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) .</span><span class="sxs-lookup"><span data-stu-id="a0091-106">Provides a method that supplements the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) interface.</span></span>

## <a name="members"></a><span data-ttu-id="a0091-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0091-107">Members</span></span>

<span data-ttu-id="a0091-108">La interfaz **IWMPControls2 (VB y C#)** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a0091-108">The **IWMPControls2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="a0091-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0091-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a0091-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0091-110">Methods</span></span>

<span data-ttu-id="a0091-111">La interfaz **IWMPControls2 (VB y C#)** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a0091-111">The **IWMPControls2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="a0091-112">Método</span><span class="sxs-lookup"><span data-stu-id="a0091-112">Method</span></span>                                                           | <span data-ttu-id="a0091-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0091-113">Description</span></span>                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0091-114">**pasar**</span><span class="sxs-lookup"><span data-stu-id="a0091-114">**step**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | <span data-ttu-id="a0091-115">Mueve el elemento multimedia de vídeo actual al siguiente fotograma o al fotograma anterior e inmoviliza la reproducción.</span><span class="sxs-lookup"><span data-stu-id="a0091-115">Moves the current video media item to the next frame or the previous frame and freezes playback.</span></span><br/> |



 

<span data-ttu-id="a0091-116">En el ejemplo de código siguiente se muestra cómo obtener acceso a una interfaz [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) .</span><span class="sxs-lookup"><span data-stu-id="a0091-116">The following example code shows how to access an [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) interface.</span></span> <span data-ttu-id="a0091-117">El código de ejemplo convierte el valor [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) que la propiedad [**AxWindowsMediaPlayer. Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) devuelve a un valor **IWMPControls2** .</span><span class="sxs-lookup"><span data-stu-id="a0091-117">The example code casts the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) value that the [**AxWindowsMediaPlayer.Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) property returns to a **IWMPControls2** value.</span></span>

<span data-ttu-id="a0091-118">Para **C#**:</span><span class="sxs-lookup"><span data-stu-id="a0091-118">For **C#**:</span></span>


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



<span data-ttu-id="a0091-119">Para **VB**:</span><span class="sxs-lookup"><span data-stu-id="a0091-119">For **VB**:</span></span>


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a><span data-ttu-id="a0091-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0091-120">Requirements</span></span>



| <span data-ttu-id="a0091-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0091-121">Requirement</span></span> | <span data-ttu-id="a0091-122">Value</span><span class="sxs-lookup"><span data-stu-id="a0091-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a0091-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0091-123">Header</span></span><br/> | <dl> <span data-ttu-id="a0091-124"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0091-124"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0091-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0091-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0091-126">**IWMPControls**</span><span class="sxs-lookup"><span data-stu-id="a0091-126">**IWMPControls**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[<span data-ttu-id="a0091-127">**Interfaces para Visual Basic .NET y C #**</span><span class="sxs-lookup"><span data-stu-id="a0091-127">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="a0091-128">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a0091-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a0091-129">**Interfaz IWMPControls3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a0091-129">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





