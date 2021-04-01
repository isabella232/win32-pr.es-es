---
title: Mensaje de LVM_SETTEXTCOLOR (commctrl. h)
description: Establece el color del texto de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetTextColor de ListView.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- LVM_SETTEXTCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150131"
---
# <a name="lvm_settextcolor-message"></a><span data-ttu-id="2cfc8-105">\_Mensaje SETTEXTCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="2cfc8-105">LVM\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="2cfc8-106">Establece el color del texto de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-106">Sets the text color of a list-view control.</span></span> <span data-ttu-id="2cfc8-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetTextColor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) .</span><span class="sxs-lookup"><span data-stu-id="2cfc8-107">You can send this message explicitly or by using the [**ListView\_SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2cfc8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cfc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cfc8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2cfc8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2cfc8-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2cfc8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2cfc8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cfc8-112">[**COLORREF**](/windows/desktop/gdi/colorref) que especifica el nuevo color de texto.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-112">A [**COLORREF**](/windows/desktop/gdi/colorref) that specifies the new text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cfc8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cfc8-113">Return value</span></span>

<span data-ttu-id="2cfc8-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2cfc8-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cfc8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cfc8-115">Requirements</span></span>



| <span data-ttu-id="2cfc8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cfc8-116">Requirement</span></span> | <span data-ttu-id="2cfc8-117">Value</span><span class="sxs-lookup"><span data-stu-id="2cfc8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cfc8-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cfc8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2cfc8-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2cfc8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2cfc8-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cfc8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2cfc8-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2cfc8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2cfc8-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cfc8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cfc8-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cfc8-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

