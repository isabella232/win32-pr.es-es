---
title: Mensaje de TDM_UPDATE_ELEMENT_TEXT (commctrl. h)
description: Actualiza un elemento de texto en un cuadro de diálogo de tarea.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6dac6787c68d0cbe619bbf28fa1a6383606e99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151141"
---
# <a name="tdm_update_element_text-message"></a><span data-ttu-id="55f03-104">\_Mensaje de \_ texto de elemento de actualización de TDM \_</span><span class="sxs-lookup"><span data-stu-id="55f03-104">TDM\_UPDATE\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="55f03-105">Actualiza un elemento de texto en un cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="55f03-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="55f03-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55f03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55f03-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55f03-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55f03-108">Indica el elemento que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="55f03-108">Indicates the element to update.</span></span> <span data-ttu-id="55f03-109">(Para ver una ilustración de los elementos, vea acerca de los [cuadros de diálogo de tareas](task-dialogs-overview.md)). Este parámetro debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="55f03-109">(For an illustration of the elements, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values:</span></span>



| <span data-ttu-id="55f03-110">Value</span><span class="sxs-lookup"><span data-stu-id="55f03-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="55f03-111">Significado</span><span class="sxs-lookup"><span data-stu-id="55f03-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="55f03-112"><dt>**contenido de TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55f03-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="55f03-113">Contenido.</span><span class="sxs-lookup"><span data-stu-id="55f03-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="55f03-114"><dt>**TDE \_ información expandida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55f03-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="55f03-115">Información expandida.</span><span class="sxs-lookup"><span data-stu-id="55f03-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="55f03-116"><dt>**pie de página de TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55f03-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="55f03-117">Texto del pie de página.</span><span class="sxs-lookup"><span data-stu-id="55f03-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="55f03-118"><dt>**\_instrucción principal de TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="55f03-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="55f03-119">Instrucción principal.</span><span class="sxs-lookup"><span data-stu-id="55f03-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="55f03-120">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55f03-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55f03-121">Puntero a una cadena Unicode que contiene el nuevo texto.</span><span class="sxs-lookup"><span data-stu-id="55f03-121">Pointer to a Unicode string that contains the new text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55f03-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55f03-122">Return value</span></span>

<span data-ttu-id="55f03-123">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="55f03-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="55f03-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55f03-124">Remarks</span></span>

<span data-ttu-id="55f03-125">Para evitar el recorte, el nuevo texto no debe ser mayor que el texto existente.</span><span class="sxs-lookup"><span data-stu-id="55f03-125">To avoid clipping, the new text must be no longer than the existing text.</span></span> <span data-ttu-id="55f03-126">Si se establece el texto en una cadena más corta, no se cambia el tamaño del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="55f03-126">Setting the text to a shorter string does not cause the dialog box to resize.</span></span>

<span data-ttu-id="55f03-127">Si el miembro **pszExpandedInformation** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizada para crear el cuadro de diálogo de tarea era **null** y se envía un mensaje de texto de **\_ \_ elemento \_ de actualización TDM** con \_ información ampliada de TDE, no se producirá \_ nada.</span><span class="sxs-lookup"><span data-stu-id="55f03-127">If the **pszExpandedInformation** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog was **NULL**, and you send a **TDM\_UPDATE\_ELEMENT\_TEXT** message with TDE\_EXPANDED\_INFORMATION, nothing will happen.</span></span>

<span data-ttu-id="55f03-128">Lo anterior también se aplica al pie de página y al pie de página de TDE \_ .</span><span class="sxs-lookup"><span data-stu-id="55f03-128">The above also applies to the footer and TDE\_FOOTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="55f03-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55f03-129">Requirements</span></span>



| <span data-ttu-id="55f03-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="55f03-130">Requirement</span></span> | <span data-ttu-id="55f03-131">Value</span><span class="sxs-lookup"><span data-stu-id="55f03-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55f03-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55f03-132">Minimum supported client</span></span><br/> | <span data-ttu-id="55f03-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="55f03-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="55f03-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55f03-134">Minimum supported server</span></span><br/> | <span data-ttu-id="55f03-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="55f03-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="55f03-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55f03-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="55f03-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55f03-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55f03-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="55f03-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f03-139">**\_texto del \_ elemento de conjunto de TDM \_**</span><span class="sxs-lookup"><span data-stu-id="55f03-139">**TDM\_SET\_ELEMENT\_TEXT**</span></span>](tdm-set-element-text.md)
</dt> </dl>

 

 





