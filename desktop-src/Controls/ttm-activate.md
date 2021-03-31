---
title: Mensaje de TTM_ACTIVATE (commctrl. h)
description: Activa o desactiva un control de información sobre herramientas.
ms.assetid: f37da001-748c-4c51-bb32-dc49031ff2fb
keywords:
- TTM_ACTIVATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_ACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e200b769cd3d9e07cb63a5a540960bcc707f862d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079392"
---
# <a name="ttm_activate-message"></a><span data-ttu-id="b8736-104">TTM \_ Activar mensaje</span><span class="sxs-lookup"><span data-stu-id="b8736-104">TTM\_ACTIVATE message</span></span>

<span data-ttu-id="b8736-105">Activa o desactiva un control de información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="b8736-105">Activates or deactivates a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8736-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8736-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8736-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8736-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8736-108">Marca de activación.</span><span class="sxs-lookup"><span data-stu-id="b8736-108">Activation flag.</span></span> <span data-ttu-id="b8736-109">Si este parámetro es **true**, se activa el control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="b8736-109">If this parameter is **TRUE**, the tooltip control is activated.</span></span> <span data-ttu-id="b8736-110">Si es **false**, se desactiva el control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="b8736-110">If it is **FALSE**, the tooltip control is deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="b8736-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8736-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b8736-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b8736-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8736-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8736-113">Return value</span></span>

<span data-ttu-id="b8736-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b8736-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8736-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8736-115">Requirements</span></span>



| <span data-ttu-id="b8736-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8736-116">Requirement</span></span> | <span data-ttu-id="b8736-117">Value</span><span class="sxs-lookup"><span data-stu-id="b8736-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8736-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8736-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8736-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b8736-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8736-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8736-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8736-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8736-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8736-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8736-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8736-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8736-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





