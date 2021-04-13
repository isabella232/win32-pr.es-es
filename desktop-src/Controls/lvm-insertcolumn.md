---
title: Mensaje de LVM_INSERTCOLUMN (commctrl. h)
description: Inserta una nueva columna en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro InsertColumn de ListView.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- LVM_INSERTCOLUMN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535032"
---
# <a name="lvm_insertcolumn-message"></a><span data-ttu-id="66864-105">\_Mensaje INSERTCOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="66864-105">LVM\_INSERTCOLUMN message</span></span>

<span data-ttu-id="66864-106">Inserta una nueva columna en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="66864-106">Inserts a new column in a list-view control.</span></span> <span data-ttu-id="66864-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ InsertColumn de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .</span><span class="sxs-lookup"><span data-stu-id="66864-107">You can send this message explicitly or by using the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="66864-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66864-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66864-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66864-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66864-110">Índice de la nueva columna.</span><span class="sxs-lookup"><span data-stu-id="66864-110">Index of the new column.</span></span>

</dd> <dt>

<span data-ttu-id="66864-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66864-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66864-112">Puntero a una estructura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contiene los atributos de la nueva columna.</span><span class="sxs-lookup"><span data-stu-id="66864-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the attributes of the new column.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66864-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66864-113">Return value</span></span>

<span data-ttu-id="66864-114">Devuelve el índice de la nueva columna si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="66864-114">Returns the index of the new column if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="66864-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66864-115">Remarks</span></span>

<span data-ttu-id="66864-116">Las columnas solo son visibles en la vista informe (detalles).</span><span class="sxs-lookup"><span data-stu-id="66864-116">Columns are visible only in report (details) view.</span></span>

## <a name="requirements"></a><span data-ttu-id="66864-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66864-117">Requirements</span></span>



| <span data-ttu-id="66864-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="66864-118">Requirement</span></span> | <span data-ttu-id="66864-119">Value</span><span class="sxs-lookup"><span data-stu-id="66864-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66864-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66864-120">Minimum supported client</span></span><br/> | <span data-ttu-id="66864-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="66864-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66864-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66864-122">Minimum supported server</span></span><br/> | <span data-ttu-id="66864-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="66864-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66864-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66864-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="66864-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66864-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





