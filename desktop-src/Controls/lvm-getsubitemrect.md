---
title: Mensaje de LVM_GETSUBITEMRECT (commctrl. h)
description: Recupera información sobre el rectángulo delimitador de un subelemento de un control de vista de lista.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- LVM_GETSUBITEMRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150889"
---
# <a name="lvm_getsubitemrect-message"></a><span data-ttu-id="f8f36-104">\_Mensaje GETSUBITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="f8f36-104">LVM\_GETSUBITEMRECT message</span></span>

<span data-ttu-id="f8f36-105">Recupera información sobre el rectángulo delimitador de un subelemento de un control de vista de lista.</span><span class="sxs-lookup"><span data-stu-id="f8f36-105">Retrieves information about the bounding rectangle for a subitem in a list-view control.</span></span> <span data-ttu-id="f8f36-106">Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetSubItemRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) (recomendado).</span><span class="sxs-lookup"><span data-stu-id="f8f36-106">You can send this message explicitly or by using the [**ListView\_GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) macro (recommended).</span></span> <span data-ttu-id="f8f36-107">Este mensaje está pensado para usarse solo con controles de vista de lista que usan el estilo de [**\_ Informe LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f8f36-107">This message is intended to be used only with list-view controls that use the [**LVS\_REPORT**](list-view-window-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8f36-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8f36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8f36-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8f36-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8f36-110">Índice del elemento primario del subelemento.</span><span class="sxs-lookup"><span data-stu-id="f8f36-110">Index of the subitem's parent item.</span></span>

</dd> <dt>

<span data-ttu-id="f8f36-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8f36-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8f36-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá la información del rectángulo delimitador del subelemento.</span><span class="sxs-lookup"><span data-stu-id="f8f36-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the subitem bounding rectangle information.</span></span> <span data-ttu-id="f8f36-113">Sus miembros se deben inicializar de acuerdo con las siguientes relaciones entre miembros y valores:</span><span class="sxs-lookup"><span data-stu-id="f8f36-113">Its members must be initialized according to the following member/value relationships:</span></span>



| <span data-ttu-id="f8f36-114">Value</span><span class="sxs-lookup"><span data-stu-id="f8f36-114">Value</span></span>                                                                                                                             | <span data-ttu-id="f8f36-115">Significado</span><span class="sxs-lookup"><span data-stu-id="f8f36-115">Meaning</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="f8f36-116"><dt>**Arriba**</dt></span><span class="sxs-lookup"><span data-stu-id="f8f36-116"><dt>**top**</dt></span></span> </dl>    | <span data-ttu-id="f8f36-117">Índice de base uno del subelemento.</span><span class="sxs-lookup"><span data-stu-id="f8f36-117">The one-based index of the subitem.</span></span><br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="f8f36-118"><dt>**salido**</dt></span><span class="sxs-lookup"><span data-stu-id="f8f36-118"><dt>**left**</dt></span></span> </dl> | <span data-ttu-id="f8f36-119">Valor de marca (vea la sección comentarios).</span><span class="sxs-lookup"><span data-stu-id="f8f36-119">Flag value (see remarks).</span></span> <span data-ttu-id="f8f36-120">Indica la parte del subelemento de vista de lista para el que se va a recuperar el rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="f8f36-120">Indicates the portion of the list-view subitem for which to retrieve the bounding rectangle.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8f36-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8f36-121">Return value</span></span>

<span data-ttu-id="f8f36-122">Devuelve un valor distinto de cero si es correcto o cero de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="f8f36-122">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8f36-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8f36-123">Remarks</span></span>

<span data-ttu-id="f8f36-124">A continuación se muestran los valores de marca que se pueden establecer.</span><span class="sxs-lookup"><span data-stu-id="f8f36-124">Following are the flag values that may be set.</span></span>



| <span data-ttu-id="f8f36-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8f36-125">Requirement</span></span> | <span data-ttu-id="f8f36-126">Value</span><span class="sxs-lookup"><span data-stu-id="f8f36-126">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f36-127">**Valor de marca**</span><span class="sxs-lookup"><span data-stu-id="f8f36-127">**Flag Value**</span></span> | <span data-ttu-id="f8f36-128">**Significado**</span><span class="sxs-lookup"><span data-stu-id="f8f36-128">**Meaning**</span></span>                                                                                                         |
| <span data-ttu-id="f8f36-129">límites de LVIR \_</span><span class="sxs-lookup"><span data-stu-id="f8f36-129">LVIR\_BOUNDS</span></span>   | <span data-ttu-id="f8f36-130">Devuelve el rectángulo delimitador del elemento completo, incluidos el icono y la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="f8f36-130">Returns the bounding rectangle of the entire item, including the icon and label.</span></span>                                    |
| <span data-ttu-id="f8f36-131">icono de LVIR \_</span><span class="sxs-lookup"><span data-stu-id="f8f36-131">LVIR\_ICON</span></span>     | <span data-ttu-id="f8f36-132">Devuelve el rectángulo delimitador del icono o del icono pequeño.</span><span class="sxs-lookup"><span data-stu-id="f8f36-132">Returns the bounding rectangle of the icon or small icon.</span></span>                                                           |
| <span data-ttu-id="f8f36-133">\_etiqueta LVIR</span><span class="sxs-lookup"><span data-stu-id="f8f36-133">LVIR\_LABEL</span></span>    | <span data-ttu-id="f8f36-134">Devuelve el rectángulo delimitador del elemento completo, incluidos el icono y la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="f8f36-134">Returns the bounding rectangle of the entire item, including the icon and label.</span></span> <span data-ttu-id="f8f36-135">Es idéntico a los límites de LVIR \_ .</span><span class="sxs-lookup"><span data-stu-id="f8f36-135">This is identical to LVIR\_BOUNDS.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f8f36-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8f36-136">Requirements</span></span>



| <span data-ttu-id="f8f36-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8f36-137">Requirement</span></span> | <span data-ttu-id="f8f36-138">Value</span><span class="sxs-lookup"><span data-stu-id="f8f36-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f36-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8f36-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f8f36-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f8f36-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8f36-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8f36-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f8f36-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8f36-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8f36-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8f36-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8f36-144"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8f36-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

