---
title: Mensaje de LVM_ARRANGE (commctrl. h)
description: Organiza los elementos en la vista de iconos. Puede enviar este mensaje explícitamente o mediante la \_ macro Arrange de ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- LVM_ARRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149908"
---
# <a name="lvm_arrange-message"></a><span data-ttu-id="f45c6-105">Mensaje de organización del LVM \_</span><span class="sxs-lookup"><span data-stu-id="f45c6-105">LVM\_ARRANGE message</span></span>

<span data-ttu-id="f45c6-106">Organiza los elementos en la vista de iconos.</span><span class="sxs-lookup"><span data-stu-id="f45c6-106">Arranges items in icon view.</span></span> <span data-ttu-id="f45c6-107">Puede enviar este mensaje explícitamente o mediante la macro [**\_ Arrange de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) .</span><span class="sxs-lookup"><span data-stu-id="f45c6-107">You can send this message explicitly or by using the [**ListView\_Arrange**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f45c6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f45c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f45c6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f45c6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f45c6-110">Uno de los siguientes valores que especifica la alineación:</span><span class="sxs-lookup"><span data-stu-id="f45c6-110">One of the following values that specifies alignment:</span></span>



| <span data-ttu-id="f45c6-111">Value</span><span class="sxs-lookup"><span data-stu-id="f45c6-111">Value</span></span>                                                                                                                                                            | <span data-ttu-id="f45c6-112">Significado</span><span class="sxs-lookup"><span data-stu-id="f45c6-112">Meaning</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <span data-ttu-id="f45c6-113"><dt>**LVA \_ ALIGNLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="f45c6-113"><dt>**LVA\_ALIGNLEFT**</dt></span></span> </dl>    | <span data-ttu-id="f45c6-114">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="f45c6-114">Not implemented.</span></span> <span data-ttu-id="f45c6-115">Aplique el [**estilo \_ ALIGNLEFT LVS**](list-view-window-styles.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f45c6-115">Apply the [**LVS\_ALIGNLEFT**](list-view-window-styles.md) style instead.</span></span><br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <span data-ttu-id="f45c6-116"><dt>**LVA \_ ALIGNTOP**</dt></span><span class="sxs-lookup"><span data-stu-id="f45c6-116"><dt>**LVA\_ALIGNTOP**</dt></span></span> </dl>       | <span data-ttu-id="f45c6-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="f45c6-117">Not implemented.</span></span> <span data-ttu-id="f45c6-118">Aplique el [**estilo \_ ALIGNTOP LVS**](list-view-window-styles.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f45c6-118">Apply the [**LVS\_ALIGNTOP**](list-view-window-styles.md) style instead.</span></span><br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <span data-ttu-id="f45c6-119"><dt>**\_valor predeterminado de LVA**</dt></span><span class="sxs-lookup"><span data-stu-id="f45c6-119"><dt>**LVA\_DEFAULT**</dt></span></span> </dl>          | <span data-ttu-id="f45c6-120">Alinea los elementos según los estilos de alineación actual del control de vista de lista (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="f45c6-120">Aligns items according to the list-view control's current alignment styles (the default value).</span></span><br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <span data-ttu-id="f45c6-121"><dt>**LVA \_ SNAPTOGRID**</dt></span><span class="sxs-lookup"><span data-stu-id="f45c6-121"><dt>**LVA\_SNAPTOGRID**</dt></span></span> </dl> | <span data-ttu-id="f45c6-122">Ajusta todos los iconos a la posición de la cuadrícula más cercana.</span><span class="sxs-lookup"><span data-stu-id="f45c6-122">Snaps all icons to the nearest grid position.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="f45c6-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f45c6-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f45c6-124">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="f45c6-124">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f45c6-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f45c6-125">Return value</span></span>

<span data-ttu-id="f45c6-126">Devuelve **true si es** correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f45c6-126">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f45c6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f45c6-127">Requirements</span></span>



| <span data-ttu-id="f45c6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f45c6-128">Requirement</span></span> | <span data-ttu-id="f45c6-129">Value</span><span class="sxs-lookup"><span data-stu-id="f45c6-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f45c6-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f45c6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f45c6-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f45c6-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f45c6-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f45c6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f45c6-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f45c6-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f45c6-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f45c6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f45c6-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f45c6-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





