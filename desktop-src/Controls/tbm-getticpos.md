---
title: Mensaje de TBM_GETTICPOS (commctrl. h)
description: Recupera la posición física actual de una marca de graduación en una barra de aumento.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- TBM_GETTICPOS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658199"
---
# <a name="tbm_getticpos-message"></a><span data-ttu-id="b86be-104">TBM \_ GETTICPOS</span><span class="sxs-lookup"><span data-stu-id="b86be-104">TBM\_GETTICPOS message</span></span>

<span data-ttu-id="b86be-105">Recupera la posición física actual de una marca de graduación en una barra de aumento.</span><span class="sxs-lookup"><span data-stu-id="b86be-105">Retrieves the current physical position of a tick mark in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b86be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b86be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b86be-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b86be-108">Índice de base cero que identifica una marca de graduación.</span><span class="sxs-lookup"><span data-stu-id="b86be-108">Zero-based index identifying a tick mark.</span></span> <span data-ttu-id="b86be-109">Las posiciones de las marcas de graduación primera y última no están directamente disponibles a través de este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b86be-109">The positions of the first and last tick marks are not directly available via this message.</span></span>

</dd> <dt>

<span data-ttu-id="b86be-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b86be-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b86be-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b86be-111">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86be-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b86be-112">Return value</span></span>

<span data-ttu-id="b86be-113">Devuelve la distancia, en coordenadas de cliente, desde el lado izquierdo o superior del área de cliente de la barra de aumento hasta la marca de graduación especificada.</span><span class="sxs-lookup"><span data-stu-id="b86be-113">Returns the distance, in client coordinates, from the left or top of the trackbar's client area to the specified tick mark.</span></span> <span data-ttu-id="b86be-114">El valor devuelto es la coordenada x de la marca de graduación de una barra de desplazamiento horizontal o la coordenada y de una barra de desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="b86be-114">The return value is the x-coordinate of the tick mark for a horizontal trackbar or the y-coordinate for a vertical trackbar.</span></span> <span data-ttu-id="b86be-115">Si *wParam* no es un índice válido, el valor devuelto es-1.</span><span class="sxs-lookup"><span data-stu-id="b86be-115">If *wParam* is not a valid index, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="b86be-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b86be-116">Remarks</span></span>

<span data-ttu-id="b86be-117">Dado que la primera y la última marca de graduación no están disponibles a través de este mensaje, los índices válidos se desplazan desde su posición de paso en la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="b86be-117">Because the first and last tick marks are not available through this message, valid indexes are offset from their tick position on the trackbar.</span></span> <span data-ttu-id="b86be-118">Si la diferencia entre [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md) y [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) es inferior a dos, no hay ningún índice válido y se producirá un error en este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b86be-118">If the difference between [**TBM\_GETRANGEMIN**](tbm-getrangemin.md) and [**TBM\_GETRANGEMAX**](tbm-getrangemax.md) is less than two, then there is no valid index and this message will fail.</span></span>

<span data-ttu-id="b86be-119">A continuación se muestra la relación entre las marcas de paso de una barra de aumento, los pasos disponibles a través de este mensaje y sus índices basados en cero.</span><span class="sxs-lookup"><span data-stu-id="b86be-119">The following illustrates the relation between the ticks on a trackbar, the ticks available through this message, and their zero-based indexes.</span></span>

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a><span data-ttu-id="b86be-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b86be-120">Requirements</span></span>



| <span data-ttu-id="b86be-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b86be-121">Requirement</span></span> | <span data-ttu-id="b86be-122">Value</span><span class="sxs-lookup"><span data-stu-id="b86be-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b86be-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b86be-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b86be-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b86be-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b86be-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b86be-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b86be-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b86be-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b86be-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b86be-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b86be-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b86be-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





