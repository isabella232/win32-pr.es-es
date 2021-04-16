---
title: Mensaje de TCM_GETCURSEL (commctrl. h)
description: Determina la pestaña seleccionada actualmente en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetCurSel.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- TCM_GETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658356"
---
# <a name="tcm_getcursel-message"></a><span data-ttu-id="f55c5-105">\_Mensaje GETCURSEL de TCM</span><span class="sxs-lookup"><span data-stu-id="f55c5-105">TCM\_GETCURSEL message</span></span>

<span data-ttu-id="f55c5-106">Determina la pestaña seleccionada actualmente en un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="f55c5-106">Determines the currently selected tab in a tab control.</span></span> <span data-ttu-id="f55c5-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="f55c5-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f55c5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f55c5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f55c5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f55c5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f55c5-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f55c5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f55c5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f55c5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f55c5-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f55c5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f55c5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f55c5-113">Return value</span></span>

<span data-ttu-id="f55c5-114">Devuelve el índice de la pestaña seleccionada si se realiza correctamente, o-1 si no hay ninguna pestaña seleccionada.</span><span class="sxs-lookup"><span data-stu-id="f55c5-114">Returns the index of the selected tab if successful, or -1 if no tab is selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="f55c5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f55c5-115">Requirements</span></span>



| <span data-ttu-id="f55c5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f55c5-116">Requirement</span></span> | <span data-ttu-id="f55c5-117">Value</span><span class="sxs-lookup"><span data-stu-id="f55c5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f55c5-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f55c5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f55c5-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f55c5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f55c5-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f55c5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f55c5-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f55c5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f55c5-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f55c5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f55c5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f55c5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





