---
title: Mensaje de HDM_INSERTITEM (commctrl. h)
description: Inserta un nuevo elemento en un control de encabezado. Puede enviar este mensaje explícitamente o utilizar el encabezado \_ InsertItem macro.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- HDM_INSERTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490709"
---
# <a name="hdm_insertitem-message"></a><span data-ttu-id="e2030-105">HDM \_ INSERTITEM Message</span><span class="sxs-lookup"><span data-stu-id="e2030-105">HDM\_INSERTITEM message</span></span>

<span data-ttu-id="e2030-106">Inserta un nuevo elemento en un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="e2030-106">Inserts a new item into a header control.</span></span> <span data-ttu-id="e2030-107">Puede enviar este mensaje explícitamente o utilizar el [**encabezado \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) macro.</span><span class="sxs-lookup"><span data-stu-id="e2030-107">You can send this message explicitly or use the [**Header\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2030-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2030-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2030-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2030-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2030-110">Índice del elemento después del cual se va a insertar el nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="e2030-110">The index of the item after which the new item is to be inserted.</span></span> <span data-ttu-id="e2030-111">El nuevo elemento se inserta al final del control de encabezado si *wParam* es mayor o igual que el número de elementos del control.</span><span class="sxs-lookup"><span data-stu-id="e2030-111">The new item is inserted at the end of the header control if *wParam* is greater than or equal to the number of items in the control.</span></span> <span data-ttu-id="e2030-112">Si *wParam* es cero, el nuevo elemento se inserta al principio del control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="e2030-112">If *wParam* is zero, the new item is inserted at the beginning of the header control.</span></span>

</dd> <dt>

<span data-ttu-id="e2030-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2030-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2030-114">Puntero a una estructura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que contiene información sobre el nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="e2030-114">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains information about the new item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2030-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2030-115">Return value</span></span>

<span data-ttu-id="e2030-116">Devuelve el índice del nuevo elemento si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e2030-116">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2030-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2030-117">Requirements</span></span>



| <span data-ttu-id="e2030-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2030-118">Requirement</span></span> | <span data-ttu-id="e2030-119">Value</span><span class="sxs-lookup"><span data-stu-id="e2030-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2030-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2030-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e2030-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e2030-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2030-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2030-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e2030-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e2030-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2030-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2030-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2030-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2030-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e2030-126">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="e2030-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e2030-127">**HDM \_ INSERTITEMW** (Unicode) y **HDM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e2030-127">**HDM\_INSERTITEMW** (Unicode) and **HDM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





