---
title: Mensaje de PGM_RECALCSIZE (commctrl. h)
description: Obliga al control de paginación a recalcular el tamaño de la ventana contenida. Al enviar este mensaje, se \_ enviará una notificación de CALCSIZE de PGN. Puede enviar este mensaje explícitamente o utilizar la macro RecalcSize de buscapersonas \_ .
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- PGM_RECALCSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490204"
---
# <a name="pgm_recalcsize-message"></a><span data-ttu-id="209e3-106">\_Mensaje RECALCSIZE PGM</span><span class="sxs-lookup"><span data-stu-id="209e3-106">PGM\_RECALCSIZE message</span></span>

<span data-ttu-id="209e3-107">Obliga al control de paginación a recalcular el tamaño de la ventana contenida.</span><span class="sxs-lookup"><span data-stu-id="209e3-107">Forces the pager control to recalculate the size of the contained window.</span></span> <span data-ttu-id="209e3-108">Al enviar este mensaje, se enviará una notificación de [ \_ CALCSIZE de PGN](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="209e3-108">Sending this message will result in a [PGN\_CALCSIZE](pgn-calcsize.md) notification being sent.</span></span> <span data-ttu-id="209e3-109">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ RecalcSize de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) .</span><span class="sxs-lookup"><span data-stu-id="209e3-109">You can send this message explicitly or use the [**Pager\_RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="209e3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="209e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="209e3-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="209e3-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="209e3-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="209e3-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="209e3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="209e3-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="209e3-114">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="209e3-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="209e3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="209e3-115">Return value</span></span>

<span data-ttu-id="209e3-116">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="209e3-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="209e3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="209e3-117">Requirements</span></span>



| <span data-ttu-id="209e3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="209e3-118">Requirement</span></span> | <span data-ttu-id="209e3-119">Value</span><span class="sxs-lookup"><span data-stu-id="209e3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="209e3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="209e3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="209e3-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="209e3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="209e3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="209e3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="209e3-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="209e3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="209e3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="209e3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="209e3-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="209e3-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





