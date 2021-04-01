---
title: Mensaje de LVM_GETNUMBEROFWORKAREAS (commctrl. h)
description: Recupera el número de áreas de trabajo en un control de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetNumberOfWorkAreas de ListView.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- LVM_GETNUMBEROFWORKAREAS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996911"
---
# <a name="lvm_getnumberofworkareas-message"></a><span data-ttu-id="8ca41-105">\_Mensaje GETNUMBEROFWORKAREAS LVM</span><span class="sxs-lookup"><span data-stu-id="8ca41-105">LVM\_GETNUMBEROFWORKAREAS message</span></span>

<span data-ttu-id="8ca41-106">Recupera el número de áreas de trabajo en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="8ca41-106">Retrieves the number of working areas in a list-view control.</span></span> <span data-ttu-id="8ca41-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetNumberOfWorkAreas de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) .</span><span class="sxs-lookup"><span data-stu-id="8ca41-107">You can send this message explicitly or use the [**ListView\_GetNumberOfWorkAreas**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ca41-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ca41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca41-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ca41-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8ca41-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8ca41-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8ca41-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ca41-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ca41-112">Puntero a un valor UINT que recibe el número de áreas de trabajo en el control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="8ca41-112">Pointer to a UINT value that receives the number of working areas in the list-view control.</span></span> <span data-ttu-id="8ca41-113">Si se coloca cero en esta variable, no se establece ninguna área de trabajo en este momento.</span><span class="sxs-lookup"><span data-stu-id="8ca41-113">If zero is placed in this variable, then no working areas are currently set.</span></span> <span data-ttu-id="8ca41-114">Este valor no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8ca41-114">This value cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca41-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ca41-115">Return value</span></span>

<span data-ttu-id="8ca41-116">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="8ca41-116">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca41-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ca41-117">Requirements</span></span>



| <span data-ttu-id="8ca41-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca41-118">Requirement</span></span> | <span data-ttu-id="8ca41-119">Value</span><span class="sxs-lookup"><span data-stu-id="8ca41-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca41-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ca41-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca41-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8ca41-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ca41-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ca41-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca41-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ca41-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ca41-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ca41-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ca41-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca41-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca41-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ca41-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca41-127">Usar controles List-View</span><span class="sxs-lookup"><span data-stu-id="8ca41-127">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 





