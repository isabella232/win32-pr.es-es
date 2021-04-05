---
title: Mensaje de TCM_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera los estilos extendidos que están actualmente en uso para el control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetExtendedStyle.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- TCM_GETEXTENDEDSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996963"
---
# <a name="tcm_getextendedstyle-message"></a><span data-ttu-id="83406-105">\_Mensaje GETEXTENDEDSTYLE de TCM</span><span class="sxs-lookup"><span data-stu-id="83406-105">TCM\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="83406-106">Recupera los estilos extendidos que están actualmente en uso para el control de ficha.</span><span class="sxs-lookup"><span data-stu-id="83406-106">Retrieves the extended styles that are currently in use for the tab control.</span></span> <span data-ttu-id="83406-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) .</span><span class="sxs-lookup"><span data-stu-id="83406-107">You can send this message explicitly or by using the [**TabCtrl\_GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="83406-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83406-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83406-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83406-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="83406-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="83406-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="83406-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83406-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="83406-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="83406-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83406-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83406-113">Return value</span></span>

<span data-ttu-id="83406-114">Devuelve un valor **DWORD** que representa los estilos extendidos actualmente en uso para el control de ficha.</span><span class="sxs-lookup"><span data-stu-id="83406-114">Returns a **DWORD** value that represents the extended styles currently in use for the tab control.</span></span> <span data-ttu-id="83406-115">Este valor es una combinación de [estilos extendidos](tab-control-extended-styles.md)de control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="83406-115">This value is a combination of tab control [extended styles](tab-control-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="83406-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83406-116">Requirements</span></span>



| <span data-ttu-id="83406-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="83406-117">Requirement</span></span> | <span data-ttu-id="83406-118">Value</span><span class="sxs-lookup"><span data-stu-id="83406-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83406-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83406-119">Minimum supported client</span></span><br/> | <span data-ttu-id="83406-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="83406-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83406-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="83406-121">Minimum supported server</span></span><br/> | <span data-ttu-id="83406-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="83406-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83406-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83406-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="83406-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="83406-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83406-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="83406-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83406-126">**\_SETEXTENDEDSTYLE TCM**</span><span class="sxs-lookup"><span data-stu-id="83406-126">**TCM\_SETEXTENDEDSTYLE**</span></span>](tcm-setextendedstyle.md)
</dt> </dl>

 

 





