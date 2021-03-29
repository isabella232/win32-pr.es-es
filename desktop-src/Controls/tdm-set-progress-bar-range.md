---
title: Mensaje de TDM_SET_PROGRESS_BAR_RANGE (commctrl. h)
description: Establece los valores mínimo y máximo de la barra de progreso en un cuadro de diálogo de tarea.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- TDM_SET_PROGRESS_BAR_RANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905640"
---
# <a name="tdm_set_progress_bar_range-message"></a><span data-ttu-id="afa8a-104">\_Mensaje de \_ intervalo de barra de progreso de configuración de \_ TDM \_</span><span class="sxs-lookup"><span data-stu-id="afa8a-104">TDM\_SET\_PROGRESS\_BAR\_RANGE message</span></span>

<span data-ttu-id="afa8a-105">Establece los valores mínimo y máximo de la barra de progreso en un cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="afa8a-105">Sets the minimum and maximum values for the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="afa8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afa8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afa8a-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="afa8a-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afa8a-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="afa8a-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="afa8a-109">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="afa8a-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afa8a-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="afa8a-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum value.</span></span> <span data-ttu-id="afa8a-111">De forma predeterminada, el valor mínimo es cero.</span><span class="sxs-lookup"><span data-stu-id="afa8a-111">By default, the minimum value is zero.</span></span> <span data-ttu-id="afa8a-112">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="afa8a-112">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum value.</span></span> <span data-ttu-id="afa8a-113">De forma predeterminada, el valor máximo es 100.</span><span class="sxs-lookup"><span data-stu-id="afa8a-113">By default, the maximum value is 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afa8a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afa8a-114">Return value</span></span>

<span data-ttu-id="afa8a-115">Devuelve los valores mínimo y máximo anteriores, si se realiza correctamente, o bien cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="afa8a-115">Returns the previous minimum and maximum values, if successful, or zero otherwise.</span></span> <span data-ttu-id="afa8a-116">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el valor mínimo y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene el valor máximo.</span><span class="sxs-lookup"><span data-stu-id="afa8a-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the minimum value, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="afa8a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afa8a-117">Requirements</span></span>



| <span data-ttu-id="afa8a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="afa8a-118">Requirement</span></span> | <span data-ttu-id="afa8a-119">Value</span><span class="sxs-lookup"><span data-stu-id="afa8a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afa8a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afa8a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="afa8a-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="afa8a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afa8a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afa8a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="afa8a-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="afa8a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afa8a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afa8a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="afa8a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="afa8a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

