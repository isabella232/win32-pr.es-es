---
title: Mensaje de LVM_GETITEMINDEXRECT (commctrl. h)
description: Recupera el rectángulo delimitador para todo o parte de un subelemento en la vista actual de un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro GetItemIndexRect de ListView.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- LVM_GETITEMINDEXRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492413"
---
# <a name="lvm_getitemindexrect-message"></a><span data-ttu-id="97471-105">\_Mensaje GETITEMINDEXRECT LVM</span><span class="sxs-lookup"><span data-stu-id="97471-105">LVM\_GETITEMINDEXRECT message</span></span>

<span data-ttu-id="97471-106">Recupera el rectángulo delimitador para todo o parte de un subelemento en la vista actual de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="97471-106">Retrieves the bounding rectangle for all or part of a subitem in the current view of a list-view control.</span></span> <span data-ttu-id="97471-107">Envíe este mensaje explícitamente o mediante la [**macro \_ GetItemIndexRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) .</span><span class="sxs-lookup"><span data-stu-id="97471-107">Send this message explicitly or by using the [**ListView\_GetItemIndexRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="97471-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97471-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97471-109">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="97471-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97471-110">Puntero a una estructura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) para el elemento primario del subelemento.</span><span class="sxs-lookup"><span data-stu-id="97471-110">A pointer to a [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the parent item of the subitem.</span></span> <span data-ttu-id="97471-111">El proceso de llamada es responsable de asignar esta estructura y establecer sus miembros.</span><span class="sxs-lookup"><span data-stu-id="97471-111">The calling process is responsible for allocating this structure and setting its members.</span></span> <span data-ttu-id="97471-112">*wParam* no debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="97471-112">*wParam* must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="97471-113">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="97471-113">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="97471-114">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) para recibir las coordenadas.</span><span class="sxs-lookup"><span data-stu-id="97471-114">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="97471-115">El proceso de llamada es responsable de la asignación de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="97471-115">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="97471-116">*lParam* no debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="97471-116">*lParam* must not be **NULL**.</span></span> <span data-ttu-id="97471-117">Establezca el miembro **superior** en el índice del subelemento.</span><span class="sxs-lookup"><span data-stu-id="97471-117">Set the **top** member to the index of the subitem.</span></span> <span data-ttu-id="97471-118">Establezca el miembro **izquierdo** en uno de los siguientes valores, que indica la parte del subelemento para el que se va a recuperar el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="97471-118">Set the **left** member to one of the following values, indicating the part of the subitem for which the bounding rectangle is to be retrieved.</span></span>



| <span data-ttu-id="97471-119">Value</span><span class="sxs-lookup"><span data-stu-id="97471-119">Value</span></span>                                                                                                                                                   | <span data-ttu-id="97471-120">Significado</span><span class="sxs-lookup"><span data-stu-id="97471-120">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <span data-ttu-id="97471-121"><dt>**límites de LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97471-121"><dt>**LVIR\_BOUNDS**</dt></span></span> </dl> | <span data-ttu-id="97471-122">Devuelve el rectángulo delimitador del subelemento completo, incluidos el icono y la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="97471-122">Returns the bounding rectangle of the entire subitem, including the icon and label.</span></span><br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <span data-ttu-id="97471-123"><dt>**icono de LVIR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="97471-123"><dt>**LVIR\_ICON**</dt></span></span> </dl>       | <span data-ttu-id="97471-124">Devuelve el rectángulo delimitador del icono o el icono pequeño del subelemento.</span><span class="sxs-lookup"><span data-stu-id="97471-124">Returns the bounding rectangle of the icon or small icon of the subitem.</span></span><br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <span data-ttu-id="97471-125"><dt>**\_etiqueta LVIR**</dt></span><span class="sxs-lookup"><span data-stu-id="97471-125"><dt>**LVIR\_LABEL**</dt></span></span> </dl>    | <span data-ttu-id="97471-126">Devuelve el rectángulo delimitador del texto del subelemento.</span><span class="sxs-lookup"><span data-stu-id="97471-126">Returns the bounding rectangle of the subitem text.</span></span><br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97471-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97471-127">Return value</span></span>

<span data-ttu-id="97471-128">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="97471-128">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="97471-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97471-129">Requirements</span></span>



| <span data-ttu-id="97471-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="97471-130">Requirement</span></span> | <span data-ttu-id="97471-131">Value</span><span class="sxs-lookup"><span data-stu-id="97471-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97471-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97471-132">Minimum supported client</span></span><br/> | <span data-ttu-id="97471-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="97471-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97471-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97471-134">Minimum supported server</span></span><br/> | <span data-ttu-id="97471-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="97471-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97471-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97471-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="97471-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97471-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

