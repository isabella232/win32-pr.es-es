---
title: Mensaje de RB_GETTOOLTIPS (commctrl. h)
description: Recupera el identificador de cualquier control de información sobre herramientas asociado al control rebar.
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- RB_GETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b500e7009ca5f5cad46dc72d5deebeebca047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150538"
---
# <a name="rb_gettooltips-message"></a><span data-ttu-id="0c837-104">Mensaje de GETTOOLTIPS de RB \_</span><span class="sxs-lookup"><span data-stu-id="0c837-104">RB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="0c837-105">Recupera el identificador de cualquier control de información sobre herramientas asociado al control rebar.</span><span class="sxs-lookup"><span data-stu-id="0c837-105">Retrieves the handle to any tooltip control associated with the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c837-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c837-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c837-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c837-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0c837-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0c837-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0c837-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c837-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0c837-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="0c837-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c837-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c837-111">Return value</span></span>

<span data-ttu-id="0c837-112">Devuelve un valor de **hWnd** que es el identificador del control de información sobre herramientas asociado al control rebar o cero si no hay ningún control de información sobre herramientas asociado al control rebar.</span><span class="sxs-lookup"><span data-stu-id="0c837-112">Returns an **HWND** value that is the handle to the tooltip control associated with the rebar control, or zero if no tooltip control is associated with the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c837-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c837-113">Requirements</span></span>



| <span data-ttu-id="0c837-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c837-114">Requirement</span></span> | <span data-ttu-id="0c837-115">Value</span><span class="sxs-lookup"><span data-stu-id="0c837-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c837-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c837-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0c837-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0c837-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c837-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c837-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0c837-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c837-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c837-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c837-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c837-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c837-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





