---
title: Mensaje de TCM_SETMINTABWIDTH (commctrl. h)
description: Establece el ancho mínimo de los elementos de un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetMinTabWidth.
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- TCM_SETMINTABWIDTH controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656460"
---
# <a name="tcm_setmintabwidth-message"></a><span data-ttu-id="694f0-105">\_Mensaje SETMINTABWIDTH de TCM</span><span class="sxs-lookup"><span data-stu-id="694f0-105">TCM\_SETMINTABWIDTH message</span></span>

<span data-ttu-id="694f0-106">Establece el ancho mínimo de los elementos de un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="694f0-106">Sets the minimum width of items in a tab control.</span></span> <span data-ttu-id="694f0-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) .</span><span class="sxs-lookup"><span data-stu-id="694f0-107">You can send this message explicitly or by using the [**TabCtrl\_SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="694f0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="694f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="694f0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="694f0-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="694f0-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="694f0-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="694f0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="694f0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="694f0-112">Ancho mínimo que se va a establecer para un elemento de control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="694f0-112">Minimum width to be set for a tab control item.</span></span> <span data-ttu-id="694f0-113">Si este parámetro se establece en-1, el control usará el ancho de tabulación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="694f0-113">If this parameter is set to -1, the control will use the default tab width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="694f0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="694f0-114">Return value</span></span>

<span data-ttu-id="694f0-115">Devuelve un valor INT que representa el ancho mínimo de tabulación anterior.</span><span class="sxs-lookup"><span data-stu-id="694f0-115">Returns an INT value that represents the previous minimum tab width.</span></span>

## <a name="requirements"></a><span data-ttu-id="694f0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="694f0-116">Requirements</span></span>



| <span data-ttu-id="694f0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="694f0-117">Requirement</span></span> | <span data-ttu-id="694f0-118">Value</span><span class="sxs-lookup"><span data-stu-id="694f0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="694f0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="694f0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="694f0-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="694f0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="694f0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="694f0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="694f0-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="694f0-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="694f0-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="694f0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="694f0-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="694f0-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





