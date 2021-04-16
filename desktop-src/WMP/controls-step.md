---
title: Controls. Step (método)
description: El método Step hace que el elemento multimedia de vídeo actual inmovilizar la reproducción en el fotograma siguiente o en el anterior.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- método de paso de Windows Media Player
- método Step Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método Step
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43fc50ea28bde95efef6e6261788fdcc62df6089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699607"
---
# <a name="controlsstep-method"></a><span data-ttu-id="c546c-106">Controls. Step (método)</span><span class="sxs-lookup"><span data-stu-id="c546c-106">Controls.step method</span></span>

<span data-ttu-id="c546c-107">El método **Step** hace que el elemento multimedia de vídeo actual inmovilizar la reproducción en el fotograma siguiente o en el anterior.</span><span class="sxs-lookup"><span data-stu-id="c546c-107">The **step** method causes the current video media item to freeze playback on the next frame or the previous frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="c546c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c546c-108">Syntax</span></span>


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a><span data-ttu-id="c546c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c546c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c546c-110">*frameCount* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c546c-110">*frameCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c546c-111">**Número** (**largo**) que indica el número de fotogramas que se van a pasar antes de la inmovilización.</span><span class="sxs-lookup"><span data-stu-id="c546c-111">**Number** (**long**) indicating how many frames to step before freezing.</span></span> <span data-ttu-id="c546c-112">Debe establecerse actualmente en 1 o-1.</span><span class="sxs-lookup"><span data-stu-id="c546c-112">Must currently be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c546c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c546c-113">Return value</span></span>

<span data-ttu-id="c546c-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c546c-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c546c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c546c-115">Remarks</span></span>

<span data-ttu-id="c546c-116">Este método solo admite actualmente los parámetros 1 o-1, por lo que solo se puede ejecutar un fotograma cada vez.</span><span class="sxs-lookup"><span data-stu-id="c546c-116">This method currently only supports the parameters 1 or -1, so you can only step one frame at a time.</span></span>

<span data-ttu-id="c546c-117">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="c546c-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="c546c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c546c-118">Requirements</span></span>



| <span data-ttu-id="c546c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c546c-119">Requirement</span></span> | <span data-ttu-id="c546c-120">Value</span><span class="sxs-lookup"><span data-stu-id="c546c-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c546c-121">Versión</span><span class="sxs-lookup"><span data-stu-id="c546c-121">Version</span></span><br/> | <span data-ttu-id="c546c-122">Windows Media Player para Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="c546c-122">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="c546c-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c546c-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c546c-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c546c-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c546c-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c546c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c546c-126">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="c546c-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="c546c-127">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="c546c-127">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





