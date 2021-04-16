---
title: Mensaje de TCM_INSERTITEM (commctrl. h)
description: Inserta una nueva pestaña en un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ InsertItem.
ms.assetid: e547c49a-699c-4137-8680-20391d138d54
keywords:
- TCM_INSERTITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_INSERTITEM
- TCM_INSERTITEMA
- TCM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58002006944a221571e37c37d25259d0aaa74fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658351"
---
# <a name="tcm_insertitem-message"></a><span data-ttu-id="f02a9-105">\_Mensaje INSERTITEM TCM</span><span class="sxs-lookup"><span data-stu-id="f02a9-105">TCM\_INSERTITEM message</span></span>

<span data-ttu-id="f02a9-106">Inserta una nueva pestaña en un control de ficha.</span><span class="sxs-lookup"><span data-stu-id="f02a9-106">Inserts a new tab in a tab control.</span></span> <span data-ttu-id="f02a9-107">Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="f02a9-107">You can send this message explicitly or by using the [**TabCtrl\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f02a9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f02a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f02a9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f02a9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f02a9-110">Índice de la nueva pestaña.</span><span class="sxs-lookup"><span data-stu-id="f02a9-110">Index of the new tab.</span></span>

</dd> <dt>

<span data-ttu-id="f02a9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f02a9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f02a9-112">Puntero a una estructura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica los atributos de la pestaña. Este mensaje omite los miembros **dwState** y **dwStateMask** de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="f02a9-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the attributes of the tab. The **dwState** and **dwStateMask** members of this structure are ignored by this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f02a9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f02a9-113">Return value</span></span>

<span data-ttu-id="f02a9-114">Devuelve el índice de la nueva pestaña si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f02a9-114">Returns the index of the new tab if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f02a9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f02a9-115">Requirements</span></span>



| <span data-ttu-id="f02a9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f02a9-116">Requirement</span></span> | <span data-ttu-id="f02a9-117">Value</span><span class="sxs-lookup"><span data-stu-id="f02a9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f02a9-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f02a9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f02a9-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f02a9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f02a9-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f02a9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f02a9-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f02a9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f02a9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f02a9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f02a9-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f02a9-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f02a9-124">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="f02a9-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f02a9-125">**TCM \_ INSERTITEMW** (Unicode) y **TCM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f02a9-125">**TCM\_INSERTITEMW** (Unicode) and **TCM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





