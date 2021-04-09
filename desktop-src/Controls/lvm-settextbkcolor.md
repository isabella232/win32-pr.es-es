---
title: Mensaje de LVM_SETTEXTBKCOLOR (commctrl. h)
description: Establece el color de fondo del texto en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetTextBkColor de ListView.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- LVM_SETTEXTBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079204"
---
# <a name="lvm_settextbkcolor-message"></a><span data-ttu-id="f177a-105">\_Mensaje SETTEXTBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="f177a-105">LVM\_SETTEXTBKCOLOR message</span></span>

<span data-ttu-id="f177a-106">Establece el color de fondo del texto en un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="f177a-106">Sets the background color of text in a list-view control.</span></span> <span data-ttu-id="f177a-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetTextBkColor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="f177a-107">You can send this message explicitly or by using the [**ListView\_SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f177a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f177a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f177a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f177a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f177a-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f177a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f177a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f177a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f177a-112">Nuevo color de fondo del texto.</span><span class="sxs-lookup"><span data-stu-id="f177a-112">New text background color.</span></span> <span data-ttu-id="f177a-113">Puede ser CLR \_ None para ningún color de fondo.</span><span class="sxs-lookup"><span data-stu-id="f177a-113">This can be CLR\_NONE for no background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f177a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f177a-114">Return value</span></span>

<span data-ttu-id="f177a-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f177a-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f177a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f177a-116">Requirements</span></span>



| <span data-ttu-id="f177a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f177a-117">Requirement</span></span> | <span data-ttu-id="f177a-118">Value</span><span class="sxs-lookup"><span data-stu-id="f177a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f177a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f177a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f177a-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f177a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f177a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f177a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f177a-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f177a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f177a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f177a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f177a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f177a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





