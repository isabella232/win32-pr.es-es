---
title: Mensaje de TCM_SETITEM (commctrl. h)
description: Establece algunos o todos los atributos de una pestaña. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ setItem.
ms.assetid: 1d9c6607-d8ec-4644-a714-22bc2677aa78
keywords:
- TCM_SETITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETITEM
- TCM_SETITEMA
- TCM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee86cd0737c3c50c89a97d3881e2cdfd3850f481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801064"
---
# <a name="tcm_setitem-message"></a><span data-ttu-id="07fd8-105">\_Mensaje SETITEM de TCM</span><span class="sxs-lookup"><span data-stu-id="07fd8-105">TCM\_SETITEM message</span></span>

<span data-ttu-id="07fd8-106">Establece algunos o todos los atributos de una pestaña.</span><span class="sxs-lookup"><span data-stu-id="07fd8-106">Sets some or all of a tab's attributes.</span></span> <span data-ttu-id="07fd8-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) .</span><span class="sxs-lookup"><span data-stu-id="07fd8-107">You can send this message explicitly or by using the [**TabCtrl\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="07fd8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07fd8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07fd8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07fd8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07fd8-110">Índice del elemento.</span><span class="sxs-lookup"><span data-stu-id="07fd8-110">Index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="07fd8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07fd8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07fd8-112">Puntero a una estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que contiene los nuevos atributos de elemento.</span><span class="sxs-lookup"><span data-stu-id="07fd8-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that contains the new item attributes.</span></span> <span data-ttu-id="07fd8-113">El miembro **Mask** especifica los atributos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="07fd8-113">The **mask** member specifies which attributes to set.</span></span> <span data-ttu-id="07fd8-114">Si el miembro **Mask** especifica el \_ valor de texto TCIF, el miembro **miembros pszText** es la dirección de una cadena terminada en NULL y se omite el miembro **cchTextMax** .</span><span class="sxs-lookup"><span data-stu-id="07fd8-114">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member is the address of a null-terminated string and the **cchTextMax** member is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07fd8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07fd8-115">Return value</span></span>

<span data-ttu-id="07fd8-116">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="07fd8-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="07fd8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07fd8-117">Requirements</span></span>



| <span data-ttu-id="07fd8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="07fd8-118">Requirement</span></span> | <span data-ttu-id="07fd8-119">Value</span><span class="sxs-lookup"><span data-stu-id="07fd8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07fd8-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07fd8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="07fd8-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="07fd8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07fd8-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="07fd8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="07fd8-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="07fd8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07fd8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07fd8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="07fd8-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="07fd8-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="07fd8-126">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="07fd8-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="07fd8-127">**TCM \_ SETITEMW** (Unicode) y **TCM \_ SETITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="07fd8-127">**TCM\_SETITEMW** (Unicode) and **TCM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





