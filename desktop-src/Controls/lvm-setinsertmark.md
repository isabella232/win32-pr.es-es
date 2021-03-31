---
title: Mensaje de LVM_SETINSERTMARK (commctrl. h)
description: Establece el punto de inserción en la posición definida.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- LVM_SETINSERTMARK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dab80b1b73b620ce94b75aecab90f6bdd69bf228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149895"
---
# <a name="lvm_setinsertmark-message"></a><span data-ttu-id="beac0-104">\_Mensaje SETINSERTMARK LVM</span><span class="sxs-lookup"><span data-stu-id="beac0-104">LVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="beac0-105">Establece el punto de inserción en la posición definida.</span><span class="sxs-lookup"><span data-stu-id="beac0-105">Sets the insertion point to the defined position.</span></span>

## <a name="parameters"></a><span data-ttu-id="beac0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="beac0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beac0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="beac0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="beac0-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="beac0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="beac0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="beac0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="beac0-110">Puntero a una estructura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> que especifica dónde se va a establecer el punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="beac0-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies where to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beac0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="beac0-111">Return value</span></span>

<span data-ttu-id="beac0-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="beac0-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="beac0-113">Se devuelve **false** si el tamaño del miembro **cbSize** de la estructura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) no es igual al tamaño real de la estructura, o cuando no se aplica un punto de inserción en la vista actual.</span><span class="sxs-lookup"><span data-stu-id="beac0-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="beac0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="beac0-114">Remarks</span></span>

<span data-ttu-id="beac0-115">Un punto de inserción solo puede aparecer si el control de vista de lista está en la vista de iconos, en la vista de iconos pequeños o en la vista de mosaico, y no en el modo de vista de grupo.</span><span class="sxs-lookup"><span data-stu-id="beac0-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="beac0-116">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="beac0-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="beac0-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="beac0-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="beac0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beac0-118">Requirements</span></span>



| <span data-ttu-id="beac0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="beac0-119">Requirement</span></span> | <span data-ttu-id="beac0-120">Value</span><span class="sxs-lookup"><span data-stu-id="beac0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="beac0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beac0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="beac0-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="beac0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="beac0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beac0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="beac0-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="beac0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="beac0-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="beac0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="beac0-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="beac0-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





