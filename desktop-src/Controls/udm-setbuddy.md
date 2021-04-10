---
title: Mensaje de UDM_SETBUDDY (commctrl. h)
description: Establece la ventana relacionada para un control de flechas.
ms.assetid: 66e35acc-95f6-4bc5-b654-690abf2188ba
keywords:
- UDM_SETBUDDY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- UDM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e8bd57727d730c67fe09a52c0bedf121eac982
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150647"
---
# <a name="udm_setbuddy-message"></a><span data-ttu-id="53790-104">\_Mensaje SETBUDDY UDM</span><span class="sxs-lookup"><span data-stu-id="53790-104">UDM\_SETBUDDY message</span></span>

<span data-ttu-id="53790-105">Establece la ventana relacionada para un control de flechas.</span><span class="sxs-lookup"><span data-stu-id="53790-105">Sets the buddy window for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="53790-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53790-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53790-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53790-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53790-108">Identificador de la nueva ventana de Buddy.</span><span class="sxs-lookup"><span data-stu-id="53790-108">Handle to the new buddy window.</span></span>

</dd> <dt>

<span data-ttu-id="53790-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53790-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="53790-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="53790-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53790-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53790-111">Return value</span></span>

<span data-ttu-id="53790-112">El valor devuelto es el identificador de la ventana relacionada anterior.</span><span class="sxs-lookup"><span data-stu-id="53790-112">The return value is the handle to the previous buddy window.</span></span>

## <a name="requirements"></a><span data-ttu-id="53790-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53790-113">Requirements</span></span>



| <span data-ttu-id="53790-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="53790-114">Requirement</span></span> | <span data-ttu-id="53790-115">Value</span><span class="sxs-lookup"><span data-stu-id="53790-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53790-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53790-116">Minimum supported client</span></span><br/> | <span data-ttu-id="53790-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="53790-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="53790-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53790-118">Minimum supported server</span></span><br/> | <span data-ttu-id="53790-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="53790-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="53790-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53790-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="53790-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53790-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





