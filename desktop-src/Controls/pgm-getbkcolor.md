---
title: Mensaje de PGM_GETBKCOLOR (commctrl. h)
description: Recupera el color de fondo actual del control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro GetBkColor de buscapersonas \_ .
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- PGM_GETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b58b139dd1caafcdefc6893e2b8a5e3312d3e28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803044"
---
# <a name="pgm_getbkcolor-message"></a><span data-ttu-id="615e0-105">\_Mensaje GETBKCOLOR PGM</span><span class="sxs-lookup"><span data-stu-id="615e0-105">PGM\_GETBKCOLOR message</span></span>

<span data-ttu-id="615e0-106">Recupera el color de fondo actual del control de paginación.</span><span class="sxs-lookup"><span data-stu-id="615e0-106">Retrieves the current background color for the pager control.</span></span> <span data-ttu-id="615e0-107">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetBkColor de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="615e0-107">You can send this message explicitly or use the [**Pager\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="615e0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="615e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="615e0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="615e0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="615e0-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="615e0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="615e0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="615e0-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="615e0-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="615e0-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="615e0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="615e0-113">Return value</span></span>

<span data-ttu-id="615e0-114">Devuelve un valor de **COLORREF** que contiene el color de fondo actual.</span><span class="sxs-lookup"><span data-stu-id="615e0-114">Returns a **COLORREF** value that contains the current background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="615e0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="615e0-115">Remarks</span></span>

<span data-ttu-id="615e0-116">De forma predeterminada, el control de paginación usará el color de la superficie del botón del sistema como color de fondo.</span><span class="sxs-lookup"><span data-stu-id="615e0-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="615e0-117">Este es el mismo color que se puede recuperar llamando a [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con el color \_ BTNFACE.</span><span class="sxs-lookup"><span data-stu-id="615e0-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="615e0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="615e0-118">Requirements</span></span>



| <span data-ttu-id="615e0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="615e0-119">Requirement</span></span> | <span data-ttu-id="615e0-120">Value</span><span class="sxs-lookup"><span data-stu-id="615e0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="615e0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="615e0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="615e0-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="615e0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="615e0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="615e0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="615e0-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="615e0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="615e0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="615e0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="615e0-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="615e0-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

