---
title: Mensaje de PGM_SETCHILD (commctrl. h)
description: Establece la ventana contenida para el control de paginación.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- PGM_SETCHILD controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150191"
---
# <a name="pgm_setchild-message"></a><span data-ttu-id="7d7c1-104">\_Mensaje SETCHILD PGM</span><span class="sxs-lookup"><span data-stu-id="7d7c1-104">PGM\_SETCHILD message</span></span>

<span data-ttu-id="7d7c1-105">Establece la ventana contenida para el control de paginación.</span><span class="sxs-lookup"><span data-stu-id="7d7c1-105">Sets the contained window for the pager control.</span></span> <span data-ttu-id="7d7c1-106">Este mensaje no cambiará el elemento primario de la ventana contenida; solo asigna un identificador de ventana al control de paginación para el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="7d7c1-106">This message will not change the parent of the contained window; it only assigns a window handle to the pager control for scrolling.</span></span> <span data-ttu-id="7d7c1-107">En la mayoría de los casos, la ventana contenida será una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="7d7c1-107">In most cases, the contained window will be a child window.</span></span> <span data-ttu-id="7d7c1-108">En este caso, la ventana contenida debe ser un elemento secundario del control de paginación.</span><span class="sxs-lookup"><span data-stu-id="7d7c1-108">If this is the case, the contained window should be a child of the pager control.</span></span> <span data-ttu-id="7d7c1-109">Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetChild de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) .</span><span class="sxs-lookup"><span data-stu-id="7d7c1-109">You can send this message explicitly or use the [**Pager\_SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d7c1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d7c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d7c1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d7c1-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7d7c1-112">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="7d7c1-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7d7c1-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d7c1-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d7c1-114">Identificador de la ventana que se va a incluir.</span><span class="sxs-lookup"><span data-stu-id="7d7c1-114">Handle to the window to be contained.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d7c1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d7c1-115">Return value</span></span>

<span data-ttu-id="7d7c1-116">No se utiliza el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="7d7c1-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d7c1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d7c1-117">Requirements</span></span>



| <span data-ttu-id="7d7c1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d7c1-118">Requirement</span></span> | <span data-ttu-id="7d7c1-119">Value</span><span class="sxs-lookup"><span data-stu-id="7d7c1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d7c1-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d7c1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7d7c1-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7d7c1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d7c1-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d7c1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7d7c1-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d7c1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d7c1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d7c1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d7c1-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d7c1-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





