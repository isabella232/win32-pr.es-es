---
title: Mensaje de TVM_SHOWINFOTIP (commctrl. h)
description: Muestra el recuadro informativo de un elemento especificado en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro ShowInfoTip de TreeView.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- TVM_SHOWINFOTIP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905639"
---
# <a name="tvm_showinfotip-message"></a><span data-ttu-id="5870b-105">\_Mensaje de SHOWINFOTIP TVM</span><span class="sxs-lookup"><span data-stu-id="5870b-105">TVM\_SHOWINFOTIP message</span></span>

<span data-ttu-id="5870b-106">Muestra el recuadro informativo de un elemento especificado en un control de vista de árbol.</span><span class="sxs-lookup"><span data-stu-id="5870b-106">Shows the infotip for a specified item in a tree-view control.</span></span> <span data-ttu-id="5870b-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ ShowInfoTip de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) .</span><span class="sxs-lookup"><span data-stu-id="5870b-107">You can send this message explicitly or by using the [**TreeView\_ShowInfoTip**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) macro..</span></span>

## <a name="parameters"></a><span data-ttu-id="5870b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5870b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5870b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5870b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5870b-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5870b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5870b-111">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5870b-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5870b-112">Identificador del elemento.</span><span class="sxs-lookup"><span data-stu-id="5870b-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5870b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5870b-113">Return value</span></span>

<span data-ttu-id="5870b-114">Devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="5870b-114">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5870b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5870b-115">Remarks</span></span>

<span data-ttu-id="5870b-116">La mayoría de las aplicaciones no usan este mensaje.</span><span class="sxs-lookup"><span data-stu-id="5870b-116">Most applications do not use this message.</span></span> <span data-ttu-id="5870b-117">Recuadros informativos se muestran automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5870b-117">Infotips are shown automatically.</span></span> <span data-ttu-id="5870b-118">Para obtener más información, vea uso de la vista de árbol recuadros informativos en la información general [sobre los controles de Tree-View](tree-view-controls.md) .</span><span class="sxs-lookup"><span data-stu-id="5870b-118">For more information, see Using Tree-view Infotips in the [About Tree-View Controls](tree-view-controls.md) overview.</span></span>

## <a name="requirements"></a><span data-ttu-id="5870b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5870b-119">Requirements</span></span>



| <span data-ttu-id="5870b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5870b-120">Requirement</span></span> | <span data-ttu-id="5870b-121">Value</span><span class="sxs-lookup"><span data-stu-id="5870b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5870b-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5870b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5870b-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5870b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5870b-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5870b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5870b-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5870b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5870b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5870b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5870b-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5870b-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





