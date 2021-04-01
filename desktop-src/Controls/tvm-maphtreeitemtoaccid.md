---
title: Mensaje de TVM_MAPHTREEITEMTOACCID (commctrl. h)
description: Asigna un HTREEITEM a un identificador de accesibilidad.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- TVM_MAPHTREEITEMTOACCID controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150299"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a><span data-ttu-id="365ed-104">\_Mensaje de MAPHTREEITEMTOACCID TVM</span><span class="sxs-lookup"><span data-stu-id="365ed-104">TVM\_MAPHTREEITEMTOACCID message</span></span>

<span data-ttu-id="365ed-105">Asigna un **HTREEITEM** a un identificador de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="365ed-105">Maps an **HTREEITEM** to an accessibility ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="365ed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="365ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="365ed-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="365ed-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="365ed-108">**HTREEITEM** que se asigna a un identificador de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="365ed-108">**HTREEITEM** that is mapped to an accessibility ID.</span></span></dd> <dt>

<span data-ttu-id="365ed-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="365ed-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="365ed-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="365ed-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="365ed-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="365ed-111">Return value</span></span>

<span data-ttu-id="365ed-112">Devuelve un identificador de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="365ed-112">Returns an accessibility ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="365ed-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="365ed-113">Remarks</span></span>

<span data-ttu-id="365ed-114">Al agregar un elemento a un control de vista de árbol, se devuelve un identificador **HTREEITEM** que identifica de forma única el elemento.</span><span class="sxs-lookup"><span data-stu-id="365ed-114">When you add an item to a tree-view control an **HTREEITEM** handle is returned that uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="365ed-115">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="365ed-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="365ed-116">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="365ed-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="365ed-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="365ed-117">Requirements</span></span>



| <span data-ttu-id="365ed-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="365ed-118">Requirement</span></span> | <span data-ttu-id="365ed-119">Value</span><span class="sxs-lookup"><span data-stu-id="365ed-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="365ed-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="365ed-120">Minimum supported client</span></span><br/> | <span data-ttu-id="365ed-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="365ed-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="365ed-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="365ed-122">Minimum supported server</span></span><br/> | <span data-ttu-id="365ed-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="365ed-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="365ed-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="365ed-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="365ed-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="365ed-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="365ed-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="365ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="365ed-127">**MapHTREEITEMtoAccID de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="365ed-127">**TreeView\_MapHTREEITEMtoAccID**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





