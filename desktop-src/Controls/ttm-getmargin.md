---
title: Mensaje de TTM_GETMARGIN (commctrl. h)
description: Recupera los márgenes superior, izquierdo, inferior y derecho establecidos para una ventana de información sobre herramientas. Un margen es la distancia, en píxeles, que hay entre el borde de la ventana de información sobre herramientas y el texto contenido dentro de la ventana de información sobre herramientas.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- TTM_GETMARGIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996413"
---
# <a name="ttm_getmargin-message"></a><span data-ttu-id="4458a-105">TTM \_ GETMARGIN</span><span class="sxs-lookup"><span data-stu-id="4458a-105">TTM\_GETMARGIN message</span></span>

<span data-ttu-id="4458a-106">Recupera los márgenes superior, izquierdo, inferior y derecho establecidos para una ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="4458a-106">Retrieves the top, left, bottom, and right margins set for a tooltip window.</span></span> <span data-ttu-id="4458a-107">Un margen es la distancia, en píxeles, que hay entre el borde de la ventana de información sobre herramientas y el texto contenido dentro de la ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="4458a-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="4458a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4458a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4458a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4458a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4458a-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4458a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4458a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4458a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4458a-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá la información del margen.</span><span class="sxs-lookup"><span data-stu-id="4458a-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the margin information.</span></span> <span data-ttu-id="4458a-113">Los miembros de la estructura **Rect** no definen un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="4458a-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="4458a-114">Para este mensaje, los miembros de la estructura se interpretan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="4458a-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="4458a-115">Value</span><span class="sxs-lookup"><span data-stu-id="4458a-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="4458a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4458a-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="4458a-117"><dt>**Arriba**</dt></span><span class="sxs-lookup"><span data-stu-id="4458a-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="4458a-118">Distancia entre el borde superior y la parte superior del texto de información sobre herramientas, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4458a-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="4458a-119"><dt>**salido**</dt></span><span class="sxs-lookup"><span data-stu-id="4458a-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="4458a-120">Distancia entre el borde izquierdo y el final izquierdo del texto de información sobre herramientas, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4458a-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="4458a-121"><dt>**descendente**</dt></span><span class="sxs-lookup"><span data-stu-id="4458a-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="4458a-122">Distancia entre el borde inferior y la parte inferior del texto de información sobre herramientas, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4458a-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="4458a-123"><dt>**correcta**</dt></span><span class="sxs-lookup"><span data-stu-id="4458a-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="4458a-124">Distancia entre el borde derecho y el extremo derecho del texto de información sobre herramientas, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="4458a-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4458a-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4458a-125">Return value</span></span>

<span data-ttu-id="4458a-126">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="4458a-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4458a-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4458a-127">Remarks</span></span>

<span data-ttu-id="4458a-128">Los cuatro márgenes tienen como valor predeterminado cero al crear el control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="4458a-128">All four margins default to zero when you create the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="4458a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4458a-129">Requirements</span></span>



| <span data-ttu-id="4458a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4458a-130">Requirement</span></span> | <span data-ttu-id="4458a-131">Value</span><span class="sxs-lookup"><span data-stu-id="4458a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4458a-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4458a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4458a-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4458a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4458a-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4458a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4458a-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4458a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4458a-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4458a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4458a-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4458a-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4458a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="4458a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4458a-139">**TTM \_ SETMARGIN**</span><span class="sxs-lookup"><span data-stu-id="4458a-139">**TTM\_SETMARGIN**</span></span>](ttm-setmargin.md)
</dt> </dl>

 

