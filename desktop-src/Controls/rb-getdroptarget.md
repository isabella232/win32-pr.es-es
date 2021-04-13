---
title: Mensaje de RB_GETDROPTARGET (commctrl. h)
description: Recupera el puntero de interfaz IDropTarget del control rebar.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- RB_GETDROPTARGET controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491764"
---
# <a name="rb_getdroptarget-message"></a><span data-ttu-id="3954f-104">Mensaje de GETDROPTARGET de RB \_</span><span class="sxs-lookup"><span data-stu-id="3954f-104">RB\_GETDROPTARGET message</span></span>

<span data-ttu-id="3954f-105">Recupera el puntero de interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) del control rebar.</span><span class="sxs-lookup"><span data-stu-id="3954f-105">Retrieves a rebar control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span>

## <a name="parameters"></a><span data-ttu-id="3954f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3954f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3954f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3954f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3954f-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3954f-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3954f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3954f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3954f-110">Puntero a un puntero [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) que recibe el puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="3954f-110">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="3954f-111">Es responsabilidad del autor de la llamada llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en este puntero cuando ya no se necesita.</span><span class="sxs-lookup"><span data-stu-id="3954f-111">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3954f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3954f-112">Return value</span></span>

<span data-ttu-id="3954f-113">No se utiliza el valor devuelto para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="3954f-113">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3954f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3954f-114">Requirements</span></span>



| <span data-ttu-id="3954f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3954f-115">Requirement</span></span> | <span data-ttu-id="3954f-116">Value</span><span class="sxs-lookup"><span data-stu-id="3954f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3954f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3954f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3954f-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3954f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3954f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3954f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3954f-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3954f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3954f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3954f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3954f-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3954f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

