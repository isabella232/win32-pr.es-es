---
title: Mensaje de TCM_HITTEST (commctrl. h)
description: Determina qué pestaña, si la hay, está en la posición de pantalla especificada. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- TCM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658352"
---
# <a name="tcm_hittest-message"></a><span data-ttu-id="6a6d7-105">\_Mensaje HITTEST de TCM</span><span class="sxs-lookup"><span data-stu-id="6a6d7-105">TCM\_HITTEST message</span></span>

<span data-ttu-id="6a6d7-106">Determina qué pestaña, si la hay, está en la posición de pantalla especificada.</span><span class="sxs-lookup"><span data-stu-id="6a6d7-106">Determines which tab, if any, is at a specified screen position.</span></span> <span data-ttu-id="6a6d7-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) .</span><span class="sxs-lookup"><span data-stu-id="6a6d7-107">You can send this message explicitly or by using the [**TabCtrl\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a6d7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a6d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a6d7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a6d7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6a6d7-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="6a6d7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6a6d7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a6d7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a6d7-112">Puntero a una estructura [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) que especifica la posición de la pantalla que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="6a6d7-112">Pointer to a [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) structure that specifies the screen position to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a6d7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a6d7-113">Return value</span></span>

<span data-ttu-id="6a6d7-114">Devuelve el índice de la pestaña o-1 si no hay ninguna tabulación en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="6a6d7-114">Returns the index of the tab, or -1 if no tab is at the specified position.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a6d7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a6d7-115">Requirements</span></span>



| <span data-ttu-id="6a6d7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a6d7-116">Requirement</span></span> | <span data-ttu-id="6a6d7-117">Value</span><span class="sxs-lookup"><span data-stu-id="6a6d7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a6d7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a6d7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6a6d7-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6a6d7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a6d7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a6d7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6a6d7-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a6d7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a6d7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a6d7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a6d7-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a6d7-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





