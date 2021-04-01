---
title: Mensaje de LVM_GETFOOTERRECT (commctrl. h)
description: Recupera las coordenadas del pie de página de un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro GetFooterRect de ListView.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- LVM_GETFOOTERRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149900"
---
# <a name="lvm_getfooterrect-message"></a><span data-ttu-id="5260f-105">\_Mensaje GETFOOTERRECT LVM</span><span class="sxs-lookup"><span data-stu-id="5260f-105">LVM\_GETFOOTERRECT message</span></span>

<span data-ttu-id="5260f-106">Recupera las coordenadas del pie de página de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="5260f-106">Retrieves the coordinates of the footer for a list-view control.</span></span> <span data-ttu-id="5260f-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetFooterRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) .</span><span class="sxs-lookup"><span data-stu-id="5260f-107">Send this message explicitly or by using the [**ListView\_GetFooterRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5260f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5260f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5260f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5260f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5260f-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5260f-110">Not used.</span></span> <span data-ttu-id="5260f-111">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="5260f-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="5260f-112">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5260f-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5260f-113">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para recibir las coordenadas.</span><span class="sxs-lookup"><span data-stu-id="5260f-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="5260f-114">El proceso de llamada es responsable de la asignación de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="5260f-114">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="5260f-115">Las coordenadas recibidas se expresan como coordenadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="5260f-115">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5260f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5260f-116">Return value</span></span>

<span data-ttu-id="5260f-117">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5260f-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5260f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5260f-118">Requirements</span></span>



| <span data-ttu-id="5260f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5260f-119">Requirement</span></span> | <span data-ttu-id="5260f-120">Value</span><span class="sxs-lookup"><span data-stu-id="5260f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5260f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5260f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5260f-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5260f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5260f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5260f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5260f-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5260f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5260f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5260f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5260f-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5260f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

