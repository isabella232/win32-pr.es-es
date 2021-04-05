---
title: Mensaje de LVM_SETWORKAREAS (commctrl. h)
description: Establece las áreas de trabajo dentro de un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetWorkAreas de ListView.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- LVM_SETWORKAREAS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996903"
---
# <a name="lvm_setworkareas-message"></a><span data-ttu-id="2ad8c-105">\_Mensaje SETWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="2ad8c-105">LVM\_SETWORKAREAS message</span></span>

<span data-ttu-id="2ad8c-106">Establece las áreas de trabajo dentro de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="2ad8c-106">Sets the working areas within a list-view control.</span></span> <span data-ttu-id="2ad8c-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetWorkAreas de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) .</span><span class="sxs-lookup"><span data-stu-id="2ad8c-107">You can send this message explicitly or use the [**ListView\_SetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ad8c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ad8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ad8c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ad8c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad8c-110">El número de estructuras de la matriz en *LPRC*.</span><span class="sxs-lookup"><span data-stu-id="2ad8c-110">The number of structures in the array at *lprc*.</span></span> <span data-ttu-id="2ad8c-111">El número máximo de áreas de trabajo permitido se define mediante el \_ valor de LV Max \_ WORKAREAS.</span><span class="sxs-lookup"><span data-stu-id="2ad8c-111">The maximum number of working areas allowed is defined by the LV\_MAX\_WORKAREAS value.</span></span>

</dd> <dt>

<span data-ttu-id="2ad8c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ad8c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad8c-113">Puntero a una matriz de estructuras [**Rect**](/previous-versions//dd162897(v=vs.85)) que contienen las nuevas áreas de trabajo del control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="2ad8c-113">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that contain the new working areas of the list-view control.</span></span> <span data-ttu-id="2ad8c-114">Los valores de estas estructuras se encuentran en coordenadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="2ad8c-114">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="2ad8c-115">Si este parámetro es **null**, el área de trabajo se establecerá en el área cliente del control.</span><span class="sxs-lookup"><span data-stu-id="2ad8c-115">If this parameter is **NULL**, the working area will be set to the client area of the control.</span></span> <span data-ttu-id="2ad8c-116">*wParam* especifica el número de estructuras de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="2ad8c-116">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ad8c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ad8c-117">Return value</span></span>

<span data-ttu-id="2ad8c-118">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="2ad8c-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ad8c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ad8c-119">Requirements</span></span>



| <span data-ttu-id="2ad8c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ad8c-120">Requirement</span></span> | <span data-ttu-id="2ad8c-121">Value</span><span class="sxs-lookup"><span data-stu-id="2ad8c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad8c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ad8c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2ad8c-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2ad8c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ad8c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ad8c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2ad8c-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ad8c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ad8c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ad8c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ad8c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ad8c-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ad8c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ad8c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ad8c-129">Usar controles List-View</span><span class="sxs-lookup"><span data-stu-id="2ad8c-129">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

