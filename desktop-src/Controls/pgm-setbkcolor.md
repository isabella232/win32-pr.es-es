---
title: Mensaje de PGM_SETBKCOLOR (commctrl. h)
description: Establece el color de fondo actual para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro SetBkColor de buscapersonas \_ .
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- PGM_SETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9e8dc1c0cad3e60bdde3f3c05d77d8c57b98ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150193"
---
# <a name="pgm_setbkcolor-message"></a><span data-ttu-id="5f124-105">\_Mensaje SETBKCOLOR PGM</span><span class="sxs-lookup"><span data-stu-id="5f124-105">PGM\_SETBKCOLOR message</span></span>

<span data-ttu-id="5f124-106">Establece el color de fondo actual para el control de paginación.</span><span class="sxs-lookup"><span data-stu-id="5f124-106">Sets the current background color for the pager control.</span></span> <span data-ttu-id="5f124-107">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetBkColor de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="5f124-107">You can send this message explicitly or use the [**Pager\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5f124-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f124-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f124-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5f124-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5f124-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5f124-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5f124-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5f124-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5f124-112">Valor de **COLORREF** que contiene el nuevo color de fondo del control de paginación.</span><span class="sxs-lookup"><span data-stu-id="5f124-112">**COLORREF** value that contains the new background color of the pager control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f124-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f124-113">Return value</span></span>

<span data-ttu-id="5f124-114">Devuelve un valor de **COLORREF** que contiene el color de fondo anterior.</span><span class="sxs-lookup"><span data-stu-id="5f124-114">Returns a **COLORREF** value that contains the previous background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f124-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f124-115">Remarks</span></span>

<span data-ttu-id="5f124-116">De forma predeterminada, el control de paginación usará el color de la superficie del botón del sistema como color de fondo.</span><span class="sxs-lookup"><span data-stu-id="5f124-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="5f124-117">Este es el mismo color que se puede recuperar llamando a [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con el color \_ BTNFACE.</span><span class="sxs-lookup"><span data-stu-id="5f124-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f124-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f124-118">Requirements</span></span>



| <span data-ttu-id="5f124-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f124-119">Requirement</span></span> | <span data-ttu-id="5f124-120">Value</span><span class="sxs-lookup"><span data-stu-id="5f124-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f124-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f124-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f124-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5f124-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5f124-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f124-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f124-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f124-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f124-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f124-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f124-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f124-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

