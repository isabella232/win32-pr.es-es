---
title: Mensaje de TDM_SET_PROGRESS_BAR_STATE (commctrl. h)
description: Establece el estado de la barra de progreso en un cuadro de diálogo de tarea.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- TDM_SET_PROGRESS_BAR_STATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f0ae4ec104c8472d3640aa804650640d77cc63
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2021
ms.locfileid: "104362006"
---
# <a name="tdm_set_progress_bar_state-message"></a><span data-ttu-id="8c431-104">Mensaje de estado de la barra de progreso del conjunto de TDM \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="8c431-104">TDM\_SET\_PROGRESS\_BAR\_STATE message</span></span>

<span data-ttu-id="8c431-105">Establece el estado de la barra de progreso en un cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="8c431-105">Sets the state of the progress bar in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c431-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c431-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c431-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c431-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c431-108">Un valor **int** que especifica el estado de la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="8c431-108">An **int** that specifies the state of the progress bar.</span></span> <span data-ttu-id="8c431-109">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8c431-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8c431-110">Valor</span><span class="sxs-lookup"><span data-stu-id="8c431-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="8c431-111">Significado</span><span class="sxs-lookup"><span data-stu-id="8c431-111">Meaning</span></span>                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <span data-ttu-id="8c431-112"><dt>**PBST \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="8c431-112"><dt>**PBST\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="8c431-113">Establece la barra de progreso en el estado normal.</span><span class="sxs-lookup"><span data-stu-id="8c431-113">Sets the progress bar to the normal state.</span></span><br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <span data-ttu-id="8c431-114"><dt>**PBST en \_ pausa**</dt></span><span class="sxs-lookup"><span data-stu-id="8c431-114"><dt>**PBST\_PAUSED**</dt></span></span> </dl>    | <span data-ttu-id="8c431-115">Establece la barra de progreso en el estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="8c431-115">Sets the progress bar to the paused state.</span></span><br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <span data-ttu-id="8c431-116"><dt>**\_error PBST**</dt></span><span class="sxs-lookup"><span data-stu-id="8c431-116"><dt>**PBST\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="8c431-117">Establezca la barra de progreso en el estado de error.</span><span class="sxs-lookup"><span data-stu-id="8c431-117">Set the progress bar to the error state.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8c431-118">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8c431-118">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c431-119">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8c431-119">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c431-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c431-120">Return value</span></span>

<span data-ttu-id="8c431-121">Si la función se ejecuta correctamente, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="8c431-121">If the function succeeds, the return value is non zero.</span></span>

<span data-ttu-id="8c431-122">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="8c431-122">If the function fails, the return value is zero.</span></span> <span data-ttu-id="8c431-123">Para obtener información de error extendida, llame a GetLastError.</span><span class="sxs-lookup"><span data-stu-id="8c431-123">To get extended error information call GetLastError.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c431-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c431-124">Requirements</span></span>



| <span data-ttu-id="8c431-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c431-125">Requirement</span></span> | <span data-ttu-id="8c431-126">Value</span><span class="sxs-lookup"><span data-stu-id="8c431-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c431-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c431-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8c431-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8c431-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c431-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c431-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8c431-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c431-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c431-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c431-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c431-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c431-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





