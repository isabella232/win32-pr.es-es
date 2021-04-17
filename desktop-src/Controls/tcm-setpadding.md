---
title: Mensaje de TCM_SETPADDING (commctrl. h)
description: Establece la cantidad de espacio (relleno) alrededor de la etiqueta y el icono de cada pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetPadding.
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656458"
---
# <a name="tcm_setpadding-message"></a><span data-ttu-id="622e2-105">\_Mensaje SETPADDING de TCM</span><span class="sxs-lookup"><span data-stu-id="622e2-105">TCM\_SETPADDING message</span></span>

<span data-ttu-id="622e2-106">Establece la cantidad de espacio (relleno) alrededor de la etiqueta y el icono de cada pestaña en un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="622e2-106">Sets the amount of space (padding) around each tab's icon and label in a tab control.</span></span> <span data-ttu-id="622e2-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) .</span><span class="sxs-lookup"><span data-stu-id="622e2-107">You can send this message explicitly or by using the [**TabCtrl\_SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="622e2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="622e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="622e2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="622e2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="622e2-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor **int** que especifica la cantidad de relleno horizontal, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="622e2-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the amount of horizontal padding, in pixels.</span></span> <span data-ttu-id="622e2-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es un valor **int** que especifica la cantidad de relleno vertical, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="622e2-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the amount of vertical padding, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="622e2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="622e2-112">Return value</span></span>

<span data-ttu-id="622e2-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="622e2-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="622e2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="622e2-114">Requirements</span></span>



| <span data-ttu-id="622e2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="622e2-115">Requirement</span></span> | <span data-ttu-id="622e2-116">Value</span><span class="sxs-lookup"><span data-stu-id="622e2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="622e2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="622e2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="622e2-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="622e2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="622e2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="622e2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="622e2-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="622e2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="622e2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="622e2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="622e2-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="622e2-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

