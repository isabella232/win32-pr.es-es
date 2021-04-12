---
title: Mensaje de LVM_GETWORKAREAS (commctrl. h)
description: Recupera las áreas de trabajo de un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetWorkAreas de ListView.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- LVM_GETWORKAREAS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492395"
---
# <a name="lvm_getworkareas-message"></a><span data-ttu-id="459c6-105">\_Mensaje GETWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="459c6-105">LVM\_GETWORKAREAS message</span></span>

<span data-ttu-id="459c6-106">Recupera las áreas de trabajo de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="459c6-106">Retrieves the working areas from a list-view control.</span></span> <span data-ttu-id="459c6-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetWorkAreas de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) .</span><span class="sxs-lookup"><span data-stu-id="459c6-107">You can send this message explicitly or use the [**ListView\_GetWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="459c6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="459c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="459c6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="459c6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="459c6-110">El número de estructuras [**Rect**](/previous-versions//dd162897(v=vs.85)) de la matriz en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="459c6-110">The number of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures in the array at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="459c6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="459c6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="459c6-112">Puntero a una matriz de estructuras [**Rect**](/previous-versions//dd162897(v=vs.85)) que reciben las áreas de trabajo actuales del control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="459c6-112">Pointer to an array of [**RECT**](/previous-versions//dd162897(v=vs.85)) structures that receive the current working areas of the list-view control.</span></span> <span data-ttu-id="459c6-113">Los valores de estas estructuras se encuentran en coordenadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="459c6-113">Values in these structures are in client coordinates.</span></span> <span data-ttu-id="459c6-114">*wParam* especifica el número de estructuras de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="459c6-114">*wParam* specifies the number of structures in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="459c6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="459c6-115">Return value</span></span>

<span data-ttu-id="459c6-116">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="459c6-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="459c6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="459c6-117">Requirements</span></span>



| <span data-ttu-id="459c6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="459c6-118">Requirement</span></span> | <span data-ttu-id="459c6-119">Value</span><span class="sxs-lookup"><span data-stu-id="459c6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="459c6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="459c6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="459c6-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="459c6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="459c6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="459c6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="459c6-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="459c6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="459c6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="459c6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="459c6-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="459c6-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="459c6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="459c6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="459c6-127">Usar controles List-View</span><span class="sxs-lookup"><span data-stu-id="459c6-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

