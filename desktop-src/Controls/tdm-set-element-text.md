---
title: TDM_SET_ELEMENT_TEXT mensaje (Commctrl.h)
description: 'TDM_SET_ELEMENT_TEXT mensaje: actualiza un elemento de texto en un cuadro de diálogo de tarea.'
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT de mensajes controles de Windows
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0c8830a6d8a1057ab283a9e096434a6184151
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104033"
---
# <a name="tdm_set_element_text-message"></a><span data-ttu-id="12ddb-104">Mensaje DE \_ TEXTO DEL ELEMENTO SET \_ \_ de TDM</span><span class="sxs-lookup"><span data-stu-id="12ddb-104">TDM\_SET\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="12ddb-105">Actualiza un elemento de texto en un cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="12ddb-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="12ddb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12ddb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ddb-107">*wParam* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="12ddb-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12ddb-108">Indica el elemento que se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="12ddb-108">Indicates the element to update.</span></span> <span data-ttu-id="12ddb-109">(Para obtener una ilustración, vea [Acerca de los cuadros de diálogo de tareas).](task-dialogs-overview.md) Este parámetro debe ser uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="12ddb-109">(For an illustration, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values.</span></span>



| <span data-ttu-id="12ddb-110">Valor</span><span class="sxs-lookup"><span data-stu-id="12ddb-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="12ddb-111">Significado</span><span class="sxs-lookup"><span data-stu-id="12ddb-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="12ddb-112"><dt>**CONTENIDO \_ de TDE**</dt></span><span class="sxs-lookup"><span data-stu-id="12ddb-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="12ddb-113">Contenido.</span><span class="sxs-lookup"><span data-stu-id="12ddb-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="12ddb-114"><dt>**INFORMACIÓN EXPANDIDA DE TDE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12ddb-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="12ddb-115">Información expandida.</span><span class="sxs-lookup"><span data-stu-id="12ddb-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="12ddb-116"><dt>**PIE DE PÁGINA DE TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12ddb-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="12ddb-117">Texto del pie de página.</span><span class="sxs-lookup"><span data-stu-id="12ddb-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="12ddb-118"><dt>**INSTRUCCIÓN PRINCIPAL DE TDE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="12ddb-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="12ddb-119">Instrucción principal.</span><span class="sxs-lookup"><span data-stu-id="12ddb-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="12ddb-120">*lParam* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="12ddb-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12ddb-121">Nuevo texto que se usará.</span><span class="sxs-lookup"><span data-stu-id="12ddb-121">The new text to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ddb-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12ddb-122">Return value</span></span>

<span data-ttu-id="12ddb-123">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="12ddb-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="12ddb-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="12ddb-124">Remarks</span></span>

<span data-ttu-id="12ddb-125">El tamaño o el diseño del cuadro de diálogo de tarea pueden cambiar para dar cabida al nuevo texto.</span><span class="sxs-lookup"><span data-stu-id="12ddb-125">The size or layout of the task dialog may change to accommodate the new text.</span></span>

## <a name="examples"></a><span data-ttu-id="12ddb-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="12ddb-126">Examples</span></span>

<span data-ttu-id="12ddb-127">El código de ejemplo siguiente muestra cómo establecer el texto del pie de página en el cuadro de diálogo de tarea representado por *hwnd*.</span><span class="sxs-lookup"><span data-stu-id="12ddb-127">The following example code shows how to set the footer text in the task dialog represented by *hwnd*.</span></span>


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a><span data-ttu-id="12ddb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12ddb-128">Requirements</span></span>



| <span data-ttu-id="12ddb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="12ddb-129">Requirement</span></span> | <span data-ttu-id="12ddb-130">Valor</span><span class="sxs-lookup"><span data-stu-id="12ddb-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12ddb-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12ddb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="12ddb-132">Solo aplicaciones de escritorio de Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="12ddb-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12ddb-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12ddb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="12ddb-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="12ddb-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12ddb-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12ddb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="12ddb-136"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="12ddb-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12ddb-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="12ddb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ddb-138">**TEXTO DEL ELEMENTO UPDATE DE TDM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12ddb-138">**TDM\_UPDATE\_ELEMENT\_TEXT**</span></span>](tdm-update-element-text.md)
</dt> </dl>

 

 





