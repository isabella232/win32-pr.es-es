---
title: Mensaje de TB_GETOBJECT (commctrl. h)
description: Recupera IDropTarget para un control de barra de herramientas.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- TB_GETOBJECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150744"
---
# <a name="tb_getobject-message"></a><span data-ttu-id="ecabd-104">\_Mensaje GETOBJECT de TB</span><span class="sxs-lookup"><span data-stu-id="ecabd-104">TB\_GETOBJECT message</span></span>

<span data-ttu-id="ecabd-105">Recupera [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) para un control de barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="ecabd-105">Retrieves the [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecabd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ecabd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecabd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecabd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecabd-108">Identificador de la interfaz que se solicita.</span><span class="sxs-lookup"><span data-stu-id="ecabd-108">Identifier of the interface being requested.</span></span> <span data-ttu-id="ecabd-109">Este valor debe apuntar al **IID \_ IDropTarget**.</span><span class="sxs-lookup"><span data-stu-id="ecabd-109">This value must point to **IID\_IDropTarget**.</span></span>

</dd> <dt>

<span data-ttu-id="ecabd-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecabd-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecabd-111">Dirección que recibe el puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="ecabd-111">Address that receives the interface pointer.</span></span> <span data-ttu-id="ecabd-112">Si se produce un error, se coloca un puntero **nulo** en esta dirección.</span><span class="sxs-lookup"><span data-stu-id="ecabd-112">If an error occurs, a **NULL** pointer is placed in this address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecabd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecabd-113">Return value</span></span>

<span data-ttu-id="ecabd-114">Devuelve un valor **HRESULT** que indica si la operación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="ecabd-114">Returns an **HRESULT** value indicating success or failure of the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecabd-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecabd-115">Remarks</span></span>

<span data-ttu-id="ecabd-116">La barra de herramientas usa el [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de la barra de herramientas cuando los objetos se arrastran o se colocan en él.</span><span class="sxs-lookup"><span data-stu-id="ecabd-116">The toolbar's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) is used by the toolbar when objects are dragged over or dropped onto it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecabd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecabd-117">Requirements</span></span>



| <span data-ttu-id="ecabd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecabd-118">Requirement</span></span> | <span data-ttu-id="ecabd-119">Value</span><span class="sxs-lookup"><span data-stu-id="ecabd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecabd-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecabd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ecabd-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ecabd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ecabd-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecabd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ecabd-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecabd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ecabd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecabd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecabd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecabd-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

