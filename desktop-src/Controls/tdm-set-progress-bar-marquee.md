---
title: Mensaje de TDM_SET_PROGRESS_BAR_MARQUEE (commctrl. h)
description: Inicia y detiene la presentación de marquesina de la barra de progreso en un cuadro de diálogo de tarea, y establece la velocidad del marco.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- TDM_SET_PROGRESS_BAR_MARQUEE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079708"
---
# <a name="tdm_set_progress_bar_marquee-message"></a><span data-ttu-id="1b36e-104">Mensaje de marquesina de la \_ \_ barra de progreso establecida \_ en TDM \_</span><span class="sxs-lookup"><span data-stu-id="1b36e-104">TDM\_SET\_PROGRESS\_BAR\_MARQUEE message</span></span>

<span data-ttu-id="1b36e-105">Inicia y detiene la presentación de marquesina de la barra de progreso en un cuadro de diálogo de tarea, y establece la velocidad del marco.</span><span class="sxs-lookup"><span data-stu-id="1b36e-105">Starts and stops the marquee display of the progress bar in a task dialog, and sets the speed of the marquee.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b36e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b36e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b36e-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1b36e-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b36e-108">Un **booleano** que indica si se debe activar o desactivar la pantalla de marquesina.</span><span class="sxs-lookup"><span data-stu-id="1b36e-108">A **BOOL** that indicates whether to turn the marquee display on or off.</span></span> <span data-ttu-id="1b36e-109">Use **true** para activar la presentación de marquesina o **false** para desactivarla.</span><span class="sxs-lookup"><span data-stu-id="1b36e-109">Use **TRUE** to turn on the marquee display, or **FALSE** to turn it off.</span></span>

</dd> <dt>

<span data-ttu-id="1b36e-110">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1b36e-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b36e-111">Un **uint** que especifica el tiempo, en milisegundos, entre las actualizaciones de la animación de marquesina.</span><span class="sxs-lookup"><span data-stu-id="1b36e-111">A **UINT** that specifies the time, in milliseconds, between marquee animation updates.</span></span> <span data-ttu-id="1b36e-112">Si este parámetro es cero, la animación de marquesina se actualiza cada 30 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="1b36e-112">If this parameter is zero, the marquee animation is updated every 30 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b36e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b36e-113">Return value</span></span>

<span data-ttu-id="1b36e-114">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1b36e-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b36e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b36e-115">Remarks</span></span>

<span data-ttu-id="1b36e-116">Para obtener información sobre el modo de marquesina, vea [control de barra de progreso](progress-bar-control.md).</span><span class="sxs-lookup"><span data-stu-id="1b36e-116">For information on marquee mode, see [Progress Bar Control](progress-bar-control.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b36e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b36e-117">Requirements</span></span>



| <span data-ttu-id="1b36e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b36e-118">Requirement</span></span> | <span data-ttu-id="1b36e-119">Value</span><span class="sxs-lookup"><span data-stu-id="1b36e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b36e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b36e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1b36e-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1b36e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b36e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b36e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1b36e-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b36e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b36e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b36e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b36e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b36e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





