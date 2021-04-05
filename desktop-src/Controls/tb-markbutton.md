---
title: Mensaje de TB_MARKBUTTON (commctrl. h)
description: Establece el estado de resaltado de un botón determinado en un control de barra de herramientas.
ms.assetid: cba0e2d2-40a7-4e20-a1ef-d5f5444c96d9
keywords:
- TB_MARKBUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_MARKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d42983f5fb0ef6e62716cefa2fa8db4fca87fa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079606"
---
# <a name="tb_markbutton-message"></a><span data-ttu-id="4bfcc-104">\_Mensaje MARKBUTTON TB</span><span class="sxs-lookup"><span data-stu-id="4bfcc-104">TB\_MARKBUTTON message</span></span>

<span data-ttu-id="4bfcc-105">Establece el estado de resaltado de un botón determinado en un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="4bfcc-105">Sets the highlight state of a given button in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4bfcc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bfcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bfcc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4bfcc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4bfcc-108">Identificador de comando para un botón de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="4bfcc-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="4bfcc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4bfcc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4bfcc-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un **booleano** que indica el nuevo estado de resaltado.</span><span class="sxs-lookup"><span data-stu-id="4bfcc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates the new highlight state.</span></span> <span data-ttu-id="4bfcc-111">Si es **true**, el botón está resaltado.</span><span class="sxs-lookup"><span data-stu-id="4bfcc-111">If **TRUE**, the button is highlighted.</span></span> <span data-ttu-id="4bfcc-112">Si es **false**, el botón se establece en su estado predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4bfcc-112">If **FALSE**, the button is set to its default state.</span></span>

<span data-ttu-id="4bfcc-113">El valor de [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4bfcc-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bfcc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bfcc-114">Return value</span></span>

<span data-ttu-id="4bfcc-115">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="4bfcc-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bfcc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bfcc-116">Requirements</span></span>



| <span data-ttu-id="4bfcc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bfcc-117">Requirement</span></span> | <span data-ttu-id="4bfcc-118">Value</span><span class="sxs-lookup"><span data-stu-id="4bfcc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfcc-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bfcc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4bfcc-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4bfcc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4bfcc-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bfcc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4bfcc-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4bfcc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4bfcc-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bfcc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bfcc-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bfcc-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

