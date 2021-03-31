---
title: Mensaje de LVM_GETGROUPRECT (commctrl. h)
description: Obtiene el rectángulo para un grupo especificado. Envíe este mensaje explícitamente o mediante la \_ macro GetGroupRect de ListView.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- LVM_GETGROUPRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2cbdfb1ec6e670e7b5d333694f3a1ca56d287b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995977"
---
# <a name="lvm_getgrouprect-message"></a><span data-ttu-id="3c7ce-105">\_Mensaje GETGROUPRECT LVM</span><span class="sxs-lookup"><span data-stu-id="3c7ce-105">LVM\_GETGROUPRECT message</span></span>

<span data-ttu-id="3c7ce-106">Obtiene el rectángulo para un grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-106">Gets the rectangle for a specified group.</span></span> <span data-ttu-id="3c7ce-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetGroupRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) .</span><span class="sxs-lookup"><span data-stu-id="3c7ce-107">Send this message explicitly or by using the [**ListView\_GetGroupRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c7ce-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c7ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c7ce-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3c7ce-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c7ce-110">Especifica el grupo por **iGroupId** (vea la estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).</span><span class="sxs-lookup"><span data-stu-id="3c7ce-110">Specifies the group by **iGroupId** (see [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure).</span></span>

</dd> <dt>

<span data-ttu-id="3c7ce-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3c7ce-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c7ce-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para recibir información sobre el grupo especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive information on the group specified by *wParam*.</span></span> <span data-ttu-id="3c7ce-113">El receptor del mensaje es responsable de establecer los miembros de la estructura con información para el grupo especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-113">The message receiver is responsible for setting the structure members with information for the group specified by *wParam*.</span></span>

<span data-ttu-id="3c7ce-114">El proceso de llamada es responsable de la asignación de memoria para la estructura.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="3c7ce-115">Establezca el miembro **superior** del [**Rect**](/previous-versions//dd162897(v=vs.85)) en una de las marcas siguientes para especificar las coordenadas del rectángulo que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-115">Set the **top** member of the [**RECT**](/previous-versions//dd162897(v=vs.85)) to one of the following flags to specify the coordinates of the rectangle to get.</span></span>



| <span data-ttu-id="3c7ce-116">Value</span><span class="sxs-lookup"><span data-stu-id="3c7ce-116">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="3c7ce-117">Significado</span><span class="sxs-lookup"><span data-stu-id="3c7ce-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <span data-ttu-id="3c7ce-118"><dt>**\_Grupo LVGGR**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7ce-118"><dt>**LVGGR\_GROUP**</dt></span></span> </dl>                | <span data-ttu-id="3c7ce-119">Coordenadas de todo el grupo expandido.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-119">Coordinates of the entire expanded group.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <span data-ttu-id="3c7ce-120"><dt>**\_encabezado LVGGR**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7ce-120"><dt>**LVGGR\_HEADER**</dt></span></span> </dl>             | <span data-ttu-id="3c7ce-121">Solo las coordenadas del encabezado (grupo contraído).</span><span class="sxs-lookup"><span data-stu-id="3c7ce-121">Coordinates of the header only (collapsed group).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <span data-ttu-id="3c7ce-122"><dt>**\_etiqueta LVGGR**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7ce-122"><dt>**LVGGR\_LABEL**</dt></span></span> </dl>                | <span data-ttu-id="3c7ce-123">Solo las coordenadas de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-123">Coordinates of the label only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <span data-ttu-id="3c7ce-124"><dt>**LVGGR \_ SUBSETLINK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7ce-124"><dt>**LVGGR\_SUBSETLINK**</dt></span></span> </dl> | <span data-ttu-id="3c7ce-125">Coordenadas solo del vínculo de subconjunto (subconjunto de marcado).</span><span class="sxs-lookup"><span data-stu-id="3c7ce-125">Coordinates of the subset link only (markup subset).</span></span> <span data-ttu-id="3c7ce-126">Un control de vista de lista puede limitar el número de elementos visibles que se muestran en cada grupo.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-126">A list-view control can limit the number of visible items displayed in each group.</span></span> <span data-ttu-id="3c7ce-127">Se presenta un vínculo al usuario para que el usuario pueda expandir el grupo.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-127">A link is presented to the user to allow the user to expand the group.</span></span> <span data-ttu-id="3c7ce-128">Esta marca devolverá el rectángulo delimitador del vínculo de subconjunto si el grupo es un subconjunto (estado de grupo de LVGS \_ subconjunto, consulte la estructura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), **Estado** miembro).</span><span class="sxs-lookup"><span data-stu-id="3c7ce-128">This flag will return the bounding rectangle of the subset link if the group is a subset (group state of LVGS\_SUBSETED, see structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), member **state**).</span></span> <span data-ttu-id="3c7ce-129">Esta marca se proporciona para que las aplicaciones de accesibilidad puedan encontrar el vínculo.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-129">This flag is provided so that accessibility applications can located the link.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c7ce-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c7ce-130">Return value</span></span>

<span data-ttu-id="3c7ce-131">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3c7ce-131">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c7ce-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c7ce-132">Requirements</span></span>



| <span data-ttu-id="3c7ce-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c7ce-133">Requirement</span></span> | <span data-ttu-id="3c7ce-134">Value</span><span class="sxs-lookup"><span data-stu-id="3c7ce-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c7ce-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c7ce-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3c7ce-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3c7ce-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c7ce-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c7ce-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3c7ce-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c7ce-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c7ce-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c7ce-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c7ce-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c7ce-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

