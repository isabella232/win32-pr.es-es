---
title: Mensaje de TCM_GETROWCOUNT (commctrl. h)
description: Recupera el número actual de filas de las fichas de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetRowCount.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- TCM_GETROWCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905547"
---
# <a name="tcm_getrowcount-message"></a><span data-ttu-id="43c69-105">\_Mensaje GETROWCOUNT de TCM</span><span class="sxs-lookup"><span data-stu-id="43c69-105">TCM\_GETROWCOUNT message</span></span>

<span data-ttu-id="43c69-106">Recupera el número actual de filas de las fichas de un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="43c69-106">Retrieves the current number of rows of tabs in a tab control.</span></span> <span data-ttu-id="43c69-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) .</span><span class="sxs-lookup"><span data-stu-id="43c69-107">You can send this message explicitly or by using the [**TabCtrl\_GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="43c69-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43c69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43c69-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43c69-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="43c69-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="43c69-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="43c69-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43c69-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="43c69-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="43c69-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43c69-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43c69-113">Return value</span></span>

<span data-ttu-id="43c69-114">Devuelve el número de filas de pestañas.</span><span class="sxs-lookup"><span data-stu-id="43c69-114">Returns the number of rows of tabs.</span></span>

## <a name="remarks"></a><span data-ttu-id="43c69-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43c69-115">Remarks</span></span>

<span data-ttu-id="43c69-116">Solo los controles de ficha que tienen el estilo de [**\_ varias líneas de TCS**](tab-control-styles.md) pueden tener varias filas de pestañas.</span><span class="sxs-lookup"><span data-stu-id="43c69-116">Only tab controls that have the [**TCS\_MULTILINE**](tab-control-styles.md) style can have multiple rows of tabs.</span></span>

## <a name="requirements"></a><span data-ttu-id="43c69-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43c69-117">Requirements</span></span>



| <span data-ttu-id="43c69-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="43c69-118">Requirement</span></span> | <span data-ttu-id="43c69-119">Value</span><span class="sxs-lookup"><span data-stu-id="43c69-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43c69-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43c69-120">Minimum supported client</span></span><br/> | <span data-ttu-id="43c69-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="43c69-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43c69-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43c69-122">Minimum supported server</span></span><br/> | <span data-ttu-id="43c69-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="43c69-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43c69-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43c69-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="43c69-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43c69-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





