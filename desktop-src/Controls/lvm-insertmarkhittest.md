---
title: Mensaje de LVM_INSERTMARKHITTEST (commctrl. h)
description: Recupera el punto de inserción más cercano a un punto especificado.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- LVM_INSERTMARKHITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150885"
---
# <a name="lvm_insertmarkhittest-message"></a><span data-ttu-id="62e53-104">\_Mensaje INSERTMARKHITTEST LVM</span><span class="sxs-lookup"><span data-stu-id="62e53-104">LVM\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="62e53-105">Recupera el punto de inserción más cercano a un punto especificado.</span><span class="sxs-lookup"><span data-stu-id="62e53-105">Retrieves the insertion point closest to a specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="62e53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62e53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62e53-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62e53-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="62e53-108">Puntero a una estructura de **punto** que contiene las coordenadas de la prueba de posicionamiento.</span><span class="sxs-lookup"><span data-stu-id="62e53-108">Pointer to a **POINT** structure that contains the hit test coordinates.</span></span></dd> <dt>

<span data-ttu-id="62e53-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62e53-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="62e53-110">Puntero a una estructura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> que especifica el punto de inserción más cercano a las coordenadas definidas por el parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="62e53-110">Pointer to an <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies the insertion point closest to the coordinates defined by the *wParam* parameter.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62e53-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62e53-111">Return value</span></span>

<span data-ttu-id="62e53-112">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="62e53-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="62e53-113">Se devuelve **false** si el tamaño del miembro **cbSize** de la estructura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) no es igual al tamaño real de la estructura, o cuando no se aplica un punto de inserción en la vista actual.</span><span class="sxs-lookup"><span data-stu-id="62e53-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="62e53-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62e53-114">Remarks</span></span>

<span data-ttu-id="62e53-115">Un punto de inserción solo puede aparecer si el control de vista de lista está en la vista de iconos, en la vista de iconos pequeños o en la vista de mosaico y no en el modo de vista de grupo.</span><span class="sxs-lookup"><span data-stu-id="62e53-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view and is not in group-view mode.</span></span>

<span data-ttu-id="62e53-116">Si los puntos de inserción no se aplican a la vista, la estructura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) contiene-1 en el miembro **iItem** .</span><span class="sxs-lookup"><span data-stu-id="62e53-116">If insertion points do not apply for the view, the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure contains a -1 in the **iItem** member.</span></span>

> [!Note]  
> <span data-ttu-id="62e53-117">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="62e53-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="62e53-118">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="62e53-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62e53-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62e53-119">Requirements</span></span>



| <span data-ttu-id="62e53-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="62e53-120">Requirement</span></span> | <span data-ttu-id="62e53-121">Value</span><span class="sxs-lookup"><span data-stu-id="62e53-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62e53-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62e53-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62e53-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="62e53-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62e53-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62e53-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62e53-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="62e53-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62e53-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62e53-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="62e53-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="62e53-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





