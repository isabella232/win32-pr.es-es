---
title: Mensaje de LVM_GETINSERTMARK (commctrl. h)
description: Recupera la posición del punto de inserción.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- LVM_GETINSERTMARK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8cba96ae7d357e3e1f5a007fa41f6b7e9e3b64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905134"
---
# <a name="lvm_getinsertmark-message"></a><span data-ttu-id="9c73b-104">\_Mensaje GETINSERTMARK LVM</span><span class="sxs-lookup"><span data-stu-id="9c73b-104">LVM\_GETINSERTMARK message</span></span>

<span data-ttu-id="9c73b-105">Recupera la posición del punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="9c73b-105">Retrieves the position of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c73b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c73b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c73b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c73b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9c73b-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9c73b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9c73b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c73b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9c73b-110">Puntero a una estructura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> que recibe la posición del punto de inserción.</span><span class="sxs-lookup"><span data-stu-id="9c73b-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that receives the position of the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c73b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c73b-111">Return value</span></span>

<span data-ttu-id="9c73b-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9c73b-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="9c73b-113">Se devuelve **false** si el tamaño del miembro **cbSize** de la estructura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) no es igual al tamaño real de la estructura.</span><span class="sxs-lookup"><span data-stu-id="9c73b-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c73b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c73b-114">Remarks</span></span>

<span data-ttu-id="9c73b-115">Un punto de inserción solo puede aparecer si el control de vista de lista está en la vista de iconos, en la vista de iconos pequeños o en la vista de mosaico, y no en el modo de vista de grupo.</span><span class="sxs-lookup"><span data-stu-id="9c73b-115">An insertion point can appear only if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="9c73b-116">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="9c73b-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="9c73b-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9c73b-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9c73b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c73b-118">Requirements</span></span>



| <span data-ttu-id="9c73b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c73b-119">Requirement</span></span> | <span data-ttu-id="9c73b-120">Value</span><span class="sxs-lookup"><span data-stu-id="9c73b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c73b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c73b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9c73b-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9c73b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c73b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c73b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9c73b-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c73b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c73b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c73b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c73b-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c73b-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





