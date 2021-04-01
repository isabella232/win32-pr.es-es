---
title: Mensaje de RB_INSERTBAND (commctrl. h)
description: Inserta una nueva banda en un control rebar.
ms.assetid: ac621f65-b8ab-41d6-928d-a48fbea572e7
keywords:
- RB_INSERTBAND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_INSERTBAND
- RB_INSERTBANDA
- RB_INSERTBANDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39b45eb662fb4c2058b87837352339c84762188
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905686"
---
# <a name="rb_insertband-message"></a><span data-ttu-id="e6d78-104">Mensaje de INSERTBAND de RB \_</span><span class="sxs-lookup"><span data-stu-id="e6d78-104">RB\_INSERTBAND message</span></span>

<span data-ttu-id="e6d78-105">Inserta una nueva banda en un control rebar.</span><span class="sxs-lookup"><span data-stu-id="e6d78-105">Inserts a new band in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6d78-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6d78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6d78-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6d78-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d78-108">Índice de base cero de la ubicación donde se insertará la banda.</span><span class="sxs-lookup"><span data-stu-id="e6d78-108">Zero-based index of the location where the band will be inserted.</span></span> <span data-ttu-id="e6d78-109">Si establece este parámetro en-1, el control agregará la nueva banda en la última ubicación.</span><span class="sxs-lookup"><span data-stu-id="e6d78-109">If you set this parameter to -1, the control will add the new band at the last location.</span></span>

</dd> <dt>

<span data-ttu-id="e6d78-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6d78-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6d78-111">Puntero a una estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que define la banda que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="e6d78-111">Pointer to a [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure that defines the band to be inserted.</span></span> <span data-ttu-id="e6d78-112">Debe establecer el miembro **cbSize** de esta estructura en **sizeof**(REBARBANDINFO) antes de enviar este mensaje.</span><span class="sxs-lookup"><span data-stu-id="e6d78-112">You must set the **cbSize** member of this structure to **sizeof**(REBARBANDINFO) before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6d78-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6d78-113">Return value</span></span>

<span data-ttu-id="e6d78-114">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="e6d78-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d78-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6d78-115">Requirements</span></span>



| <span data-ttu-id="e6d78-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6d78-116">Requirement</span></span> | <span data-ttu-id="e6d78-117">Value</span><span class="sxs-lookup"><span data-stu-id="e6d78-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d78-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6d78-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e6d78-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e6d78-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6d78-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6d78-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e6d78-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6d78-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6d78-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6d78-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6d78-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6d78-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="e6d78-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="e6d78-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e6d78-125">**RB \_ INSERTBANDW** (Unicode) y **RB \_ INSERTBANDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e6d78-125">**RB\_INSERTBANDW** (Unicode) and **RB\_INSERTBANDA** (ANSI)</span></span><br/>               |



 

 





