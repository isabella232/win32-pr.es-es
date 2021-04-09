---
title: Mensaje de TDM_SET_ELEMENT_TEXT (commctrl. h)
description: Actualiza un elemento de texto en un cuadro de diálogo de tarea.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT controles de mensajes de Windows
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
ms.openlocfilehash: 2229dc269f14c9a3b0765675dcc97dc9776b72c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079709"
---
# <a name="tdm_set_element_text-message"></a><span data-ttu-id="5ec53-104">\_Mensaje de \_ texto del elemento de conjunto de TDM \_</span><span class="sxs-lookup"><span data-stu-id="5ec53-104">TDM\_SET\_ELEMENT\_TEXT message</span></span>

<span data-ttu-id="5ec53-105">Actualiza un elemento de texto en un cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="5ec53-105">Updates a text element in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="5ec53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ec53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ec53-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ec53-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec53-108">Indica el elemento que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="5ec53-108">Indicates the element to update.</span></span> <span data-ttu-id="5ec53-109">(Para ver una ilustración, consulte Acerca de los [cuadros de diálogo de tareas](task-dialogs-overview.md)). Este parámetro debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5ec53-109">(For an illustration, see [About Task Dialogs](task-dialogs-overview.md).) This parameter must be one of the following values.</span></span>



| <span data-ttu-id="5ec53-110">Value</span><span class="sxs-lookup"><span data-stu-id="5ec53-110">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="5ec53-111">Significado</span><span class="sxs-lookup"><span data-stu-id="5ec53-111">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <span data-ttu-id="5ec53-112"><dt>**contenido de TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ec53-112"><dt>**TDE\_CONTENT**</dt></span></span> </dl>                                         | <span data-ttu-id="5ec53-113">Contenido.</span><span class="sxs-lookup"><span data-stu-id="5ec53-113">Content.</span></span><br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <span data-ttu-id="5ec53-114"><dt>**TDE \_ información expandida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ec53-114"><dt>**TDE\_EXPANDED\_INFORMATION**</dt></span></span> </dl> | <span data-ttu-id="5ec53-115">Información expandida.</span><span class="sxs-lookup"><span data-stu-id="5ec53-115">Expanded information.</span></span><br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <span data-ttu-id="5ec53-116"><dt>**pie de página de TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ec53-116"><dt>**TDE\_FOOTER**</dt></span></span> </dl>                                            | <span data-ttu-id="5ec53-117">Texto del pie de página.</span><span class="sxs-lookup"><span data-stu-id="5ec53-117">Footer text.</span></span><br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <span data-ttu-id="5ec53-118"><dt>**\_instrucción principal de TDE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5ec53-118"><dt>**TDE\_MAIN\_INSTRUCTION**</dt></span></span> </dl>             | <span data-ttu-id="5ec53-119">Instrucción principal.</span><span class="sxs-lookup"><span data-stu-id="5ec53-119">Main instruction.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="5ec53-120">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ec53-120">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ec53-121">Nuevo texto que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="5ec53-121">The new text to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ec53-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ec53-122">Return value</span></span>

<span data-ttu-id="5ec53-123">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="5ec53-123">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ec53-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ec53-124">Remarks</span></span>

<span data-ttu-id="5ec53-125">El tamaño o el diseño del cuadro de diálogo de la tarea puede cambiar para dar cabida al nuevo texto.</span><span class="sxs-lookup"><span data-stu-id="5ec53-125">The size or layout of the task dialog may change to accommodate the new text.</span></span>

## <a name="examples"></a><span data-ttu-id="5ec53-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5ec53-126">Examples</span></span>

<span data-ttu-id="5ec53-127">En el ejemplo de código siguiente se muestra cómo establecer el texto del pie de página en el cuadro de diálogo de tarea representado por *hWnd*.</span><span class="sxs-lookup"><span data-stu-id="5ec53-127">The following example code shows how to set the footer text in the task dialog represented by *hwnd*.</span></span>


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a><span data-ttu-id="5ec53-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ec53-128">Requirements</span></span>



| <span data-ttu-id="5ec53-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ec53-129">Requirement</span></span> | <span data-ttu-id="5ec53-130">Value</span><span class="sxs-lookup"><span data-stu-id="5ec53-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec53-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ec53-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5ec53-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5ec53-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5ec53-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ec53-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5ec53-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ec53-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5ec53-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ec53-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ec53-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ec53-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec53-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ec53-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec53-138">**\_texto del \_ elemento de actualización de TDM \_**</span><span class="sxs-lookup"><span data-stu-id="5ec53-138">**TDM\_UPDATE\_ELEMENT\_TEXT**</span></span>](tdm-update-element-text.md)
</dt> </dl>

 

 





