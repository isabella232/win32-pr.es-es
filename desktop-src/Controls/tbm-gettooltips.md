---
title: Mensaje de TBM_GETTOOLTIPS (commctrl. h)
description: Recupera el identificador del control de información sobre herramientas asignado a TrackBar, si existe.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- TBM_GETTOOLTIPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905258"
---
# <a name="tbm_gettooltips-message"></a><span data-ttu-id="c8e6b-104">TBM \_ GETTOOLTIPS</span><span class="sxs-lookup"><span data-stu-id="c8e6b-104">TBM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="c8e6b-105">Recupera el identificador del control de información sobre herramientas asignado a TrackBar, si existe.</span><span class="sxs-lookup"><span data-stu-id="c8e6b-105">Retrieves the handle to the tooltip control assigned to the trackbar, if any.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8e6b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8e6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8e6b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8e6b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c8e6b-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c8e6b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c8e6b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8e6b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c8e6b-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c8e6b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8e6b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8e6b-111">Return value</span></span>

<span data-ttu-id="c8e6b-112">Devuelve el identificador del control de información sobre herramientas asignado a TrackBar o **null** si la información sobre herramientas no está en uso.</span><span class="sxs-lookup"><span data-stu-id="c8e6b-112">Returns the handle to the tooltip control assigned to the trackbar, or **NULL** if tooltips are not in use.</span></span> <span data-ttu-id="c8e6b-113">Si el control TrackBar no usa el estilo [**de \_ información sobre herramientas de TBS**](trackbar-control-styles.md) , el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="c8e6b-113">If the trackbar control does not use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8e6b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8e6b-114">Requirements</span></span>



| <span data-ttu-id="c8e6b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8e6b-115">Requirement</span></span> | <span data-ttu-id="c8e6b-116">Value</span><span class="sxs-lookup"><span data-stu-id="c8e6b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e6b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8e6b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c8e6b-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c8e6b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8e6b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8e6b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c8e6b-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8e6b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8e6b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8e6b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8e6b-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8e6b-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





