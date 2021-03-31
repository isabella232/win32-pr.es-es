---
title: Mensaje de STM_GETICON (Winuser. h)
description: Una aplicación envía el \_ mensaje STM GETICON para recuperar un identificador del icono asociado a un control estático que tiene el estilo de \_ icono SS.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- STM_GETICON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150016"
---
# <a name="stm_geticon-message"></a><span data-ttu-id="926c6-104">\_Mensaje GETICON de STM</span><span class="sxs-lookup"><span data-stu-id="926c6-104">STM\_GETICON message</span></span>

<span data-ttu-id="926c6-105">Una aplicación envía el mensaje **STM \_ GETICON** para recuperar un identificador del icono asociado a un control estático que tiene el estilo de \_ icono SS.</span><span class="sxs-lookup"><span data-stu-id="926c6-105">An application sends the **STM\_GETICON** message to retrieve a handle to the icon associated with a static control that has the SS\_ICON style.</span></span>

## <a name="parameters"></a><span data-ttu-id="926c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="926c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="926c6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="926c6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="926c6-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="926c6-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="926c6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="926c6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="926c6-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="926c6-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="926c6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="926c6-111">Return value</span></span>

<span data-ttu-id="926c6-112">El valor devuelto es un identificador del icono o **null** si el control estático no tiene ningún icono asociado o si se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="926c6-112">The return value is a handle to the icon, or **NULL** if either the static control has no associated icon or if an error occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="926c6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="926c6-113">Requirements</span></span>



| <span data-ttu-id="926c6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="926c6-114">Requirement</span></span> | <span data-ttu-id="926c6-115">Value</span><span class="sxs-lookup"><span data-stu-id="926c6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="926c6-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="926c6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="926c6-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="926c6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="926c6-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="926c6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="926c6-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="926c6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="926c6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="926c6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="926c6-121"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="926c6-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="926c6-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="926c6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="926c6-123">**STM \_ SETICON**</span><span class="sxs-lookup"><span data-stu-id="926c6-123">**STM\_SETICON**</span></span>](stm-seticon.md)
</dt> </dl>

 

 





