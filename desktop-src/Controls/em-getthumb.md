---
title: Mensaje de EM_GETTHUMB (Winuser. h)
description: Obtiene la posición del cuadro de desplazamiento (Thumb) en la barra de desplazamiento vertical de un control de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 04bd0102-1652-405b-8c42-50e138abaf75
keywords:
- EM_GETTHUMB controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETTHUMB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6689c530794e11897f1f88a7d5864058d53aa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150763"
---
# <a name="em_getthumb-message"></a><span data-ttu-id="736b6-105">\_Mensaje GETTHUMB em</span><span class="sxs-lookup"><span data-stu-id="736b6-105">EM\_GETTHUMB message</span></span>

<span data-ttu-id="736b6-106">Obtiene la posición del cuadro de desplazamiento (Thumb) en la barra de desplazamiento vertical de un control de edición multilínea.</span><span class="sxs-lookup"><span data-stu-id="736b6-106">Gets the position of the scroll box (thumb) in the vertical scroll bar of a multiline edit control.</span></span> <span data-ttu-id="736b6-107">Puede enviar este mensaje a un control de edición o a un control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="736b6-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="736b6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="736b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="736b6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="736b6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="736b6-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="736b6-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="736b6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="736b6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="736b6-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="736b6-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="736b6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="736b6-113">Return value</span></span>

<span data-ttu-id="736b6-114">El valor devuelto es la posición del cuadro de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="736b6-114">The return value is the position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="736b6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="736b6-115">Remarks</span></span>

<span data-ttu-id="736b6-116">**Edición enriquecida:** Compatible con Microsoft Rich Edit 2,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="736b6-116">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="736b6-117">Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="736b6-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="736b6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="736b6-118">Requirements</span></span>



| <span data-ttu-id="736b6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="736b6-119">Requirement</span></span> | <span data-ttu-id="736b6-120">Value</span><span class="sxs-lookup"><span data-stu-id="736b6-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="736b6-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="736b6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="736b6-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="736b6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="736b6-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="736b6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="736b6-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="736b6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="736b6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="736b6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="736b6-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="736b6-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





