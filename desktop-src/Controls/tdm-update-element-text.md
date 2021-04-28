---
title: TDM_UPDATE_ELEMENT_TEXT mensaje (Commctrl.h)
description: 'TDM_UPDATE_ELEMENT_TEXT mensaje: actualiza un elemento de texto en un cuadro de diálogo de tarea.'
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT de mensajes controles de Windows
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
ms.openlocfilehash: c155b426b92645c0b9cdbabe00c44ffa722b89f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085813"
---
# <a name="tdm_update_element_text-message"></a><span data-ttu-id="416d8-104">Mensaje DE \_ TEXTO DEL ELEMENTO UPDATE \_ \_ de TDM</span><span class="sxs-lookup"><span data-stu-id="416d8-104">TDM\_UPDATE\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="416d8-105">Actualiza un elemento de texto en un cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="416d8-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="416d8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="416d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="416d8-107">*wParam* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="416d8-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="416d8-108">Indica el elemento que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="416d8-108">Indicates the element to update.</span></span> <span data-ttu-id="416d8-109">(Para obtener una ilustración de los elementos, vea [Acerca de los cuadros de diálogo de tarea).](task-dialogs-overview.md) Este parámetro debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="416d8-109">(For an illustration of the elements, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values:</span></span>



| <span data-ttu-id="416d8-110">Valor</span><span class="sxs-lookup"><span data-stu-id="416d8-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="416d8-111">Significado</span><span class="sxs-lookup"><span data-stu-id="416d8-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="416d8-112"><dt>**CONTENIDO \_ de TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="416d8-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="416d8-113">Contenido.</span><span class="sxs-lookup"><span data-stu-id="416d8-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="416d8-114"><dt>**INFORMACIÓN EXPANDIDA DE TDE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="416d8-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="416d8-115">Información expandida.</span><span class="sxs-lookup"><span data-stu-id="416d8-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="416d8-116"><dt>**PIE DE PÁGINA DE TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="416d8-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="416d8-117">Texto del pie de página.</span><span class="sxs-lookup"><span data-stu-id="416d8-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="416d8-118"><dt>**INSTRUCCIÓN PRINCIPAL DE TDE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="416d8-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="416d8-119">Instrucción principal.</span><span class="sxs-lookup"><span data-stu-id="416d8-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="416d8-120">*lParam* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="416d8-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="416d8-121">Puntero a una cadena Unicode que contiene el nuevo texto.</span><span class="sxs-lookup"><span data-stu-id="416d8-121">Pointer to a Unicode string that contains the new text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="416d8-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="416d8-122">Return value</span></span>

<span data-ttu-id="416d8-123">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="416d8-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="416d8-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="416d8-124">Remarks</span></span>

<span data-ttu-id="416d8-125">Para evitar el recorte, el nuevo texto no debe ser mayor que el texto existente.</span><span class="sxs-lookup"><span data-stu-id="416d8-125">To avoid clipping, the new text must be no longer than the existing text.</span></span> <span data-ttu-id="416d8-126">Establecer el texto en una cadena más corta no hace que el cuadro de diálogo cambie de tamaño.</span><span class="sxs-lookup"><span data-stu-id="416d8-126">Setting the text to a shorter string does not cause the dialog box to resize.</span></span>

<span data-ttu-id="416d8-127">Si el miembro **pszExpandedInformation** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usada para crear el cuadro de diálogo de tarea era **NULL** y envía un mensaje **\_ TDM UPDATE \_ ELEMENT \_ TEXT** con TDE \_ EXPANDED INFORMATION, no ocurrirá \_ nada.</span><span class="sxs-lookup"><span data-stu-id="416d8-127">If the **pszExpandedInformation** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog was **NULL**, and you send a **TDM\_UPDATE\_ELEMENT\_TEXT** message with TDE\_EXPANDED\_INFORMATION, nothing will happen.</span></span>

<span data-ttu-id="416d8-128">Lo anterior también se aplica al pie de página y al pie de página de \_ TDE.</span><span class="sxs-lookup"><span data-stu-id="416d8-128">The above also applies to the footer and TDE\_FOOTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="416d8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="416d8-129">Requirements</span></span>



| <span data-ttu-id="416d8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="416d8-130">Requirement</span></span> | <span data-ttu-id="416d8-131">Valor</span><span class="sxs-lookup"><span data-stu-id="416d8-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="416d8-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="416d8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="416d8-133">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="416d8-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="416d8-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="416d8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="416d8-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="416d8-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="416d8-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="416d8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="416d8-137"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="416d8-137"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="416d8-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="416d8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416d8-139">**TEXTO DEL \_ ELEMENTO SET \_ DE TDM \_**</span><span class="sxs-lookup"><span data-stu-id="416d8-139">**TDM\_SET\_ELEMENT\_TEXT**</span></span>](tdm-set-element-text.md)
</dt> </dl>

 

 





