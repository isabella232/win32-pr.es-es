---
title: IWMPControls2 Step (método)
description: El método Step hace que el elemento multimedia de vídeo actual se desplazará al fotograma siguiente o al fotograma anterior e inmovilizará la reproducción.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- método de paso de Windows Media Player
- método de paso Windows Media Player, interfaz IWMPControls2
- Interfaz IWMPControls2 Windows Media Player, método Step
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690871"
---
# <a name="iwmpcontrols2step-method"></a><span data-ttu-id="dbe84-106">IWMPControls2:: Step (método)</span><span class="sxs-lookup"><span data-stu-id="dbe84-106">IWMPControls2::step method</span></span>

<span data-ttu-id="dbe84-107">El método **Step** hace que el elemento multimedia de vídeo actual se desplazará al fotograma siguiente o al fotograma anterior e inmovilizará la reproducción.</span><span class="sxs-lookup"><span data-stu-id="dbe84-107">The **step** method causes the current video media item to step to the next frame or the previous frame and freeze playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe84-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbe84-108">Syntax</span></span>


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a><span data-ttu-id="dbe84-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dbe84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbe84-110">*lStep* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dbe84-110">*lStep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbe84-111">Un valor **System. Int32** que indica el número de fotogramas que se van a pasar antes de la inmovilización.</span><span class="sxs-lookup"><span data-stu-id="dbe84-111">A **System.Int32** value indicating how many frames to step before freezing.</span></span> <span data-ttu-id="dbe84-112">Debe establecerse en 1 o-1.</span><span class="sxs-lookup"><span data-stu-id="dbe84-112">Must be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbe84-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dbe84-113">Return value</span></span>

<span data-ttu-id="dbe84-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="dbe84-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbe84-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbe84-115">Remarks</span></span>

<span data-ttu-id="dbe84-116">Actualmente, este método solo admite los parámetros 1 o-1, por lo que solo se puede ejecutar un fotograma cada vez.</span><span class="sxs-lookup"><span data-stu-id="dbe84-116">This method currently supports only the parameters 1 or -1, so you can only step one frame at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe84-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbe84-117">Requirements</span></span>



| <span data-ttu-id="dbe84-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbe84-118">Requirement</span></span> | <span data-ttu-id="dbe84-119">Value</span><span class="sxs-lookup"><span data-stu-id="dbe84-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe84-120">Versión</span><span class="sxs-lookup"><span data-stu-id="dbe84-120">Version</span></span><br/>   | <span data-ttu-id="dbe84-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="dbe84-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dbe84-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dbe84-122">Namespace</span></span><br/> | <span data-ttu-id="dbe84-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dbe84-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dbe84-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="dbe84-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dbe84-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dbe84-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe84-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbe84-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe84-127">**Interfaz IWMPControls2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dbe84-127">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbe84-128">**Interfaz IWMPDVD (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dbe84-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





