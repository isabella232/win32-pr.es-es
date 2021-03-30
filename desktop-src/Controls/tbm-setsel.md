---
title: Mensaje de TBM_SETSEL (commctrl. h)
description: Establece las posiciones inicial y final para el intervalo de selección disponible en una barra de inicio.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- TBM_SETSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edebc6b6dcf3b0b93e3047a39aac74c34d121bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801076"
---
# <a name="tbm_setsel-message"></a><span data-ttu-id="238d8-104">TBM \_ SETSEL</span><span class="sxs-lookup"><span data-stu-id="238d8-104">TBM\_SETSEL message</span></span>

<span data-ttu-id="238d8-105">Establece las posiciones inicial y final para el intervalo de selección disponible en una barra de inicio.</span><span class="sxs-lookup"><span data-stu-id="238d8-105">Sets the starting and ending positions for the available selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="238d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="238d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="238d8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="238d8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="238d8-108">Volver a dibujar el marcador.</span><span class="sxs-lookup"><span data-stu-id="238d8-108">Redraw flag.</span></span> <span data-ttu-id="238d8-109">Si este parámetro es **true**, el mensaje vuelve a dibujar el TrackBar después de establecer el intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="238d8-109">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="238d8-110">Si este parámetro es **false**, el mensaje establece el intervalo de selección, pero no vuelve a dibujar el TrackBar.</span><span class="sxs-lookup"><span data-stu-id="238d8-110">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="238d8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="238d8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="238d8-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la posición lógica de inicio para el intervalo de selección y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición lógica final.</span><span class="sxs-lookup"><span data-stu-id="238d8-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the starting logical position for the selection range, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the ending logical position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="238d8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="238d8-113">Return value</span></span>

<span data-ttu-id="238d8-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="238d8-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="238d8-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="238d8-115">Remarks</span></span>

<span data-ttu-id="238d8-116">Este mensaje se omite si TrackBar no tiene el estilo [**\_ ENABLESELRANGE de TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="238d8-116">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

<span data-ttu-id="238d8-117">**TBM \_ SETSEL** le permite restringir el puntero a solo una parte del intervalo disponible en la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="238d8-117">**TBM\_SETSEL** allows you to restrict the pointer to only a portion of the range available to the progress bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="238d8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="238d8-118">Requirements</span></span>



| <span data-ttu-id="238d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="238d8-119">Requirement</span></span> | <span data-ttu-id="238d8-120">Value</span><span class="sxs-lookup"><span data-stu-id="238d8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="238d8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="238d8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="238d8-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="238d8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="238d8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="238d8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="238d8-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="238d8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="238d8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="238d8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="238d8-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="238d8-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="238d8-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="238d8-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="238d8-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="238d8-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="238d8-129">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="238d8-129">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="238d8-130">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="238d8-130">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="238d8-131">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="238d8-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="238d8-132">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="238d8-132">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

