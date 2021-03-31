---
title: Mensaje de HDM_DELETEITEM (commctrl. h)
description: Elimina un elemento de un control de encabezado. Puede enviar este mensaje explícitamente o utilizar la \_ macro DeleteItem de encabezado.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- HDM_DELETEITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079529"
---
# <a name="hdm_deleteitem-message"></a><span data-ttu-id="8f6c4-105">Mensaje de HDM \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="8f6c4-105">HDM\_DELETEITEM message</span></span>

<span data-ttu-id="8f6c4-106">Elimina un elemento de un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-106">Deletes an item from a header control.</span></span> <span data-ttu-id="8f6c4-107">Puede enviar este mensaje explícitamente o utilizar la [**macro \_ DeleteItem de encabezado**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="8f6c4-107">You can send this message explicitly or use the [**Header\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f6c4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f6c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f6c4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f6c4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f6c4-110">Índice del elemento que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-110">An index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="8f6c4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f6c4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8f6c4-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f6c4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f6c4-113">Return value</span></span>

<span data-ttu-id="8f6c4-114">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8f6c4-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f6c4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f6c4-115">Requirements</span></span>



| <span data-ttu-id="8f6c4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f6c4-116">Requirement</span></span> | <span data-ttu-id="8f6c4-117">Value</span><span class="sxs-lookup"><span data-stu-id="8f6c4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f6c4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f6c4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8f6c4-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8f6c4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f6c4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f6c4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8f6c4-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8f6c4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f6c4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f6c4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f6c4-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f6c4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





