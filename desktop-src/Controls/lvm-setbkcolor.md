---
title: Mensaje de LVM_SETBKCOLOR (commctrl. h)
description: Establece el color de fondo de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetBkColor de ListView.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- LVM_SETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996644"
---
# <a name="lvm_setbkcolor-message"></a><span data-ttu-id="e315a-105">\_Mensaje SETBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="e315a-105">LVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="e315a-106">Establece el color de fondo de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="e315a-106">Sets the background color of a list-view control.</span></span> <span data-ttu-id="e315a-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetBkColor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="e315a-107">You can send this message explicitly or by using the [**ListView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e315a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e315a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e315a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e315a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e315a-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="e315a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e315a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e315a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e315a-112">Color de fondo que se va a establecer o el \_ valor NONE de CLR para ningún color de fondo.</span><span class="sxs-lookup"><span data-stu-id="e315a-112">Background color to set or the CLR\_NONE value for no background color.</span></span> <span data-ttu-id="e315a-113">Los controles de vista de lista con colores de fondo se vuelven a dibujar con mayor rapidez que los que no tienen colores de fondo.</span><span class="sxs-lookup"><span data-stu-id="e315a-113">List-view controls with background colors redraw themselves significantly faster than those without background colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e315a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e315a-114">Return value</span></span>

<span data-ttu-id="e315a-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e315a-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e315a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e315a-116">Requirements</span></span>



| <span data-ttu-id="e315a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e315a-117">Requirement</span></span> | <span data-ttu-id="e315a-118">Value</span><span class="sxs-lookup"><span data-stu-id="e315a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e315a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e315a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e315a-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e315a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e315a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e315a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e315a-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e315a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e315a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e315a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e315a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e315a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





