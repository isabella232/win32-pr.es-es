---
title: Mensaje de LVM_APPROXIMATEVIEWRECT (commctrl. h)
description: Calcula el ancho y el alto aproximados necesarios para mostrar un número determinado de elementos. Puede enviar este mensaje explícitamente o utilizar la \_ macro ApproximateViewRect de ListView.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- LVM_APPROXIMATEVIEWRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be929d34acad46b75a53a9e0cc8825ec9801e998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995943"
---
# <a name="lvm_approximateviewrect-message"></a><span data-ttu-id="fedda-105">\_Mensaje APPROXIMATEVIEWRECT LVM</span><span class="sxs-lookup"><span data-stu-id="fedda-105">LVM\_APPROXIMATEVIEWRECT message</span></span>

<span data-ttu-id="fedda-106">Calcula el ancho y el alto aproximados necesarios para mostrar un número determinado de elementos.</span><span class="sxs-lookup"><span data-stu-id="fedda-106">Calculates the approximate width and height required to display a given number of items.</span></span> <span data-ttu-id="fedda-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ ApproximateViewRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) .</span><span class="sxs-lookup"><span data-stu-id="fedda-107">You can send this message explicitly or use the [**ListView\_ApproximateViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fedda-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fedda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fedda-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fedda-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fedda-110">Número de elementos que se van a mostrar en el control.</span><span class="sxs-lookup"><span data-stu-id="fedda-110">The number of items to be displayed in the control.</span></span> <span data-ttu-id="fedda-111">Si este parámetro se establece en-1, el mensaje utiliza el número total de elementos del control.</span><span class="sxs-lookup"><span data-stu-id="fedda-111">If this parameter is set to -1, the message uses the total number of items in the control.</span></span>

</dd> <dt>

<span data-ttu-id="fedda-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fedda-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fedda-113">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es la dimensión x propuesta del control, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fedda-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the proposed x-dimension of the control, in pixels.</span></span> <span data-ttu-id="fedda-114">Este parámetro se puede establecer en-1 para permitir que el mensaje use el valor de ancho actual.</span><span class="sxs-lookup"><span data-stu-id="fedda-114">This parameter can be set to -1 to allow the message to use the current width value.</span></span>

<span data-ttu-id="fedda-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es la dimensión y propuesta del control, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fedda-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the proposed y-dimension of the control, in pixels.</span></span> <span data-ttu-id="fedda-116">Este parámetro se puede establecer en-1 para permitir que el mensaje use el valor del alto actual.</span><span class="sxs-lookup"><span data-stu-id="fedda-116">This parameter can be set to -1 to allow the message to use the current height value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fedda-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fedda-117">Return value</span></span>

<span data-ttu-id="fedda-118">Devuelve un valor **DWORD** que contiene el ancho aproximado (en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) y el alto (en [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) necesarios para mostrar los elementos, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fedda-118">Returns a **DWORD** value that holds the approximate width (in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) and height (in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) needed to display the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="fedda-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fedda-119">Remarks</span></span>

<span data-ttu-id="fedda-120">Establecer el tamaño del control de vista de lista en función de las dimensiones proporcionadas por este mensaje puede optimizar el redibujo y reducir el parpadeo.</span><span class="sxs-lookup"><span data-stu-id="fedda-120">Setting the size of the list-view control based on the dimensions provided by this message can optimize redraw and reduce flicker.</span></span>

## <a name="requirements"></a><span data-ttu-id="fedda-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fedda-121">Requirements</span></span>



| <span data-ttu-id="fedda-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fedda-122">Requirement</span></span> | <span data-ttu-id="fedda-123">Value</span><span class="sxs-lookup"><span data-stu-id="fedda-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fedda-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fedda-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fedda-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fedda-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fedda-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fedda-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fedda-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fedda-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fedda-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fedda-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fedda-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fedda-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

