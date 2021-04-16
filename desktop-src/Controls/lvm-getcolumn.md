---
title: Mensaje de LVM_GETCOLUMN (commctrl. h)
description: Obtiene los atributos de la columna de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro getcolumn (de ListView.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- LVM_GETCOLUMN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489065"
---
# <a name="lvm_getcolumn-message"></a><span data-ttu-id="4104e-105">\_Mensaje GETCOLUMN (LVM</span><span class="sxs-lookup"><span data-stu-id="4104e-105">LVM\_GETCOLUMN message</span></span>

<span data-ttu-id="4104e-106">Obtiene los atributos de la columna de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="4104e-106">Gets the attributes of a list-view control's column.</span></span> <span data-ttu-id="4104e-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ Getcolumn (de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) .</span><span class="sxs-lookup"><span data-stu-id="4104e-107">You can send this message explicitly or by using the [**ListView\_GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4104e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4104e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4104e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4104e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4104e-110">Índice de la columna.</span><span class="sxs-lookup"><span data-stu-id="4104e-110">The index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="4104e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4104e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4104e-112">Puntero a una estructura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que especifica la información que se va a recuperar y recibe información sobre la columna.</span><span class="sxs-lookup"><span data-stu-id="4104e-112">A pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that specifies the information to retrieve and receives information about the column.</span></span> <span data-ttu-id="4104e-113">El miembro **Mask** especifica los atributos de columna que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="4104e-113">The **mask** member specifies which column attributes to retrieve.</span></span> <span data-ttu-id="4104e-114">Si el miembro **Mask** especifica el \_ valor de texto LVCF, el miembro **miembros pszText** debe contener la dirección del búfer que recibe el texto del elemento y el miembro **cchTextMax** debe especificar el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="4104e-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4104e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4104e-115">Return value</span></span>

<span data-ttu-id="4104e-116">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4104e-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4104e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4104e-117">Requirements</span></span>



| <span data-ttu-id="4104e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4104e-118">Requirement</span></span> | <span data-ttu-id="4104e-119">Value</span><span class="sxs-lookup"><span data-stu-id="4104e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4104e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4104e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4104e-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4104e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4104e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4104e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4104e-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4104e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4104e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4104e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4104e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4104e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





