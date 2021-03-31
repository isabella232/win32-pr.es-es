---
title: Mensaje de TB_GETTOOLTIPS (commctrl. h)
description: Recupera el identificador del control de información sobre herramientas, si existe, asociado a la barra de herramientas.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- TB_GETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488212b34f9f1816797f097a5a1f42d2ea4f68c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079454"
---
# <a name="tb_gettooltips-message"></a><span data-ttu-id="80349-104">\_Mensaje GETTOOLTIPS TB</span><span class="sxs-lookup"><span data-stu-id="80349-104">TB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="80349-105">Recupera el identificador del control de información sobre herramientas, si existe, asociado a la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="80349-105">Retrieves the handle to the tooltip control, if any, associated with the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="80349-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80349-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80349-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80349-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="80349-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="80349-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="80349-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80349-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="80349-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="80349-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80349-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80349-111">Return value</span></span>

<span data-ttu-id="80349-112">Devuelve el identificador del control ToolTip o **null** si la barra de herramientas no tiene información sobre herramientas asociada.</span><span class="sxs-lookup"><span data-stu-id="80349-112">Returns the handle to the tooltip control, or **NULL** if the toolbar has no associated tooltip.</span></span>

## <a name="requirements"></a><span data-ttu-id="80349-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80349-113">Requirements</span></span>



| <span data-ttu-id="80349-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="80349-114">Requirement</span></span> | <span data-ttu-id="80349-115">Value</span><span class="sxs-lookup"><span data-stu-id="80349-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80349-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80349-116">Minimum supported client</span></span><br/> | <span data-ttu-id="80349-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="80349-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="80349-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80349-118">Minimum supported server</span></span><br/> | <span data-ttu-id="80349-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="80349-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80349-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80349-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="80349-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="80349-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





