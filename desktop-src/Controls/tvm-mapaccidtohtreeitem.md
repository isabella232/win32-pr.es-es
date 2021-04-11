---
title: Mensaje de TVM_MAPACCIDTOHTREEITEM (commctrl. h)
description: Asigna un identificador de accesibilidad a un HTREEITEM.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- TVM_MAPACCIDTOHTREEITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079110"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a><span data-ttu-id="5568d-104">\_Mensaje de MAPACCIDTOHTREEITEM TVM</span><span class="sxs-lookup"><span data-stu-id="5568d-104">TVM\_MAPACCIDTOHTREEITEM message</span></span>

<span data-ttu-id="5568d-105">Asigna un identificador de accesibilidad a un **HTREEITEM**.</span><span class="sxs-lookup"><span data-stu-id="5568d-105">Maps an accessibility ID to an **HTREEITEM**.</span></span>

## <a name="parameters"></a><span data-ttu-id="5568d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5568d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5568d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5568d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5568d-108">**Uint** que contiene el identificador de accesibilidad que se va a asignar a un **HTREEITEM**.</span><span class="sxs-lookup"><span data-stu-id="5568d-108">**UINT** that contains the accessibility ID to map to an **HTREEITEM**.</span></span> </dd> <dt>

<span data-ttu-id="5568d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5568d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5568d-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5568d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5568d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5568d-111">Return value</span></span>

<span data-ttu-id="5568d-112">Devuelve el **HTREEITEM** al que está asignado el identificador de accesibilidad especificado.</span><span class="sxs-lookup"><span data-stu-id="5568d-112">Returns the **HTREEITEM** that the specified accessibility ID is mapped to.</span></span>

## <a name="remarks"></a><span data-ttu-id="5568d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5568d-113">Remarks</span></span>

<span data-ttu-id="5568d-114">Al agregar un elemento a un control de vista de árbol, un **HTREEITEM** devuelve, que identifica de forma única el elemento.</span><span class="sxs-lookup"><span data-stu-id="5568d-114">When you add an item to a tree-view control an **HTREEITEM** returns, which uniquely identifies the item.</span></span>

> [!Note]  
> <span data-ttu-id="5568d-115">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="5568d-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5568d-116">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5568d-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5568d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5568d-117">Requirements</span></span>



| <span data-ttu-id="5568d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5568d-118">Requirement</span></span> | <span data-ttu-id="5568d-119">Value</span><span class="sxs-lookup"><span data-stu-id="5568d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5568d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5568d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5568d-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5568d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5568d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5568d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5568d-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5568d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5568d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5568d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5568d-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5568d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5568d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5568d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5568d-127">**MapAccIDToHTREEITEM de TreeView \_**</span><span class="sxs-lookup"><span data-stu-id="5568d-127">**TreeView\_MapAccIDToHTREEITEM**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





