---
title: Mensaje de TTM_SETMARGIN (commctrl. h)
description: Establece los márgenes superior, izquierdo, inferior y derecho de una ventana de información sobre herramientas. Un margen es la distancia, en píxeles, que hay entre el borde de la ventana de información sobre herramientas y el texto contenido dentro de la ventana de información sobre herramientas.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- TTM_SETMARGIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed46bf40833a3046d15386782897eb6b573b29c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658185"
---
# <a name="ttm_setmargin-message"></a><span data-ttu-id="83b59-105">TTM \_ SETMARGIN Message</span><span class="sxs-lookup"><span data-stu-id="83b59-105">TTM\_SETMARGIN message</span></span>

<span data-ttu-id="83b59-106">Establece los márgenes superior, izquierdo, inferior y derecho de una ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="83b59-106">Sets the top, left, bottom, and right margins for a tooltip window.</span></span> <span data-ttu-id="83b59-107">Un margen es la distancia, en píxeles, que hay entre el borde de la ventana de información sobre herramientas y el texto contenido dentro de la ventana de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="83b59-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="83b59-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83b59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83b59-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83b59-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="83b59-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="83b59-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="83b59-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83b59-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83b59-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contiene la información de margen que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="83b59-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margin information to be set.</span></span> <span data-ttu-id="83b59-113">Los miembros de la estructura **Rect** no definen un rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="83b59-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="83b59-114">Para este mensaje, los miembros de la estructura se interpretan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="83b59-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="83b59-115">Value</span><span class="sxs-lookup"><span data-stu-id="83b59-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="83b59-116">Significado</span><span class="sxs-lookup"><span data-stu-id="83b59-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="83b59-117"><dt>**Arriba**</dt></span><span class="sxs-lookup"><span data-stu-id="83b59-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="83b59-118">Distancia entre el borde superior y la parte superior del texto de información sobre herramientas, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="83b59-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="83b59-119"><dt>**salido**</dt></span><span class="sxs-lookup"><span data-stu-id="83b59-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="83b59-120">Distancia entre el borde izquierdo y el final izquierdo del texto de información sobre herramientas, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="83b59-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="83b59-121"><dt>**descendente**</dt></span><span class="sxs-lookup"><span data-stu-id="83b59-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="83b59-122">Distancia entre el borde inferior y la parte inferior del texto de información sobre herramientas, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="83b59-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="83b59-123"><dt>**correcta**</dt></span><span class="sxs-lookup"><span data-stu-id="83b59-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="83b59-124">Distancia entre el borde derecho y el extremo derecho del texto de información sobre herramientas, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="83b59-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83b59-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83b59-125">Return value</span></span>

<span data-ttu-id="83b59-126">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="83b59-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="83b59-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83b59-127">Remarks</span></span>

<span data-ttu-id="83b59-128">Este mensaje no tiene ningún efecto cuando la aplicación se ejecuta en Windows Vista y los estilos visuales están habilitados para la información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="83b59-128">This message has no effect when the application runs on Windows Vista and visual styles are enabled for the tooltip.</span></span> <span data-ttu-id="83b59-129">Puede deshabilitar los estilos visuales para la información sobre herramientas mediante [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span><span class="sxs-lookup"><span data-stu-id="83b59-129">You can disable visual styles for the tooltip by using [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span></span>

## <a name="requirements"></a><span data-ttu-id="83b59-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83b59-130">Requirements</span></span>



| <span data-ttu-id="83b59-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="83b59-131">Requirement</span></span> | <span data-ttu-id="83b59-132">Value</span><span class="sxs-lookup"><span data-stu-id="83b59-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83b59-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83b59-133">Minimum supported client</span></span><br/> | <span data-ttu-id="83b59-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="83b59-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83b59-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83b59-135">Minimum supported server</span></span><br/> | <span data-ttu-id="83b59-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="83b59-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83b59-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83b59-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="83b59-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83b59-138"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83b59-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="83b59-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b59-140">**TTM \_ GETMARGIN**</span><span class="sxs-lookup"><span data-stu-id="83b59-140">**TTM\_GETMARGIN**</span></span>](ttm-getmargin.md)
</dt> </dl>

 

