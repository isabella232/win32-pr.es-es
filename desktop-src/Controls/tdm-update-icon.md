---
title: Mensaje de TDM_UPDATE_ICON (commctrl. h)
description: Actualiza el icono de un cuadro de diálogo de tarea.
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- TDM_UPDATE_ICON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997108"
---
# <a name="tdm_update_icon-message"></a><span data-ttu-id="718ea-104">Mensaje de icono de \_ actualización de TDM \_</span><span class="sxs-lookup"><span data-stu-id="718ea-104">TDM\_UPDATE\_ICON message</span></span>

<span data-ttu-id="718ea-105">Actualiza el icono de un cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="718ea-105">Refreshes the icon of a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="718ea-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="718ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="718ea-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="718ea-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="718ea-108">Indica qué elemento de icono se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="718ea-108">Indicates which icon element to update.</span></span> <span data-ttu-id="718ea-109">Este parámetro debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="718ea-109">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="718ea-110">Value</span><span class="sxs-lookup"><span data-stu-id="718ea-110">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="718ea-111">Significado</span><span class="sxs-lookup"><span data-stu-id="718ea-111">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <span data-ttu-id="718ea-112"><dt>**icono de TDIE \_ \_ Main**</dt></span><span class="sxs-lookup"><span data-stu-id="718ea-112"><dt>**TDIE\_ICON\_MAIN**</dt></span></span> </dl>       | <span data-ttu-id="718ea-113">Icono principal.</span><span class="sxs-lookup"><span data-stu-id="718ea-113">Main icon.</span></span><br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <span data-ttu-id="718ea-114"><dt>**TDIE \_ icono de \_ pie de página**</dt></span><span class="sxs-lookup"><span data-stu-id="718ea-114"><dt>**TDIE\_ICON\_FOOTER**</dt></span></span> </dl> | <span data-ttu-id="718ea-115">Icono de pie de página.</span><span class="sxs-lookup"><span data-stu-id="718ea-115">Footer icon.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="718ea-116">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="718ea-116">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="718ea-117">Un puntero a una cadena (PCWSTR) o un identificador a un icono (HICON) que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="718ea-117">A pointer to a string (PCWSTR) or handle to an icon (HICON) to display.</span></span> <span data-ttu-id="718ea-118">Si *lParam* es **null**, no se muestra ningún icono, independientemente del valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="718ea-118">If *lParam* is **NULL**, no icon is displayed, regardless of the value of *wParam*.</span></span>

<span data-ttu-id="718ea-119">Si el valor de *wParam* es TDIE \_ Icon \_ Main y la \_ marca TDF use \_ HICON \_ Main se establece en el miembro **dwFlags** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizada para crear el cuadro de diálogo de tarea, *lParam* debe contener un identificador de un icono (HICON) que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="718ea-119">If the value of *wParam* is TDIE\_ICON\_MAIN and the TDF\_USE\_HICON\_MAIN flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="718ea-120">Si el valor de *wParam* es TDIE \_ Icon \_ footer y la marca TDF \_ use \_ HICON \_ footer está establecida en el miembro **dwFlags** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizada para crear el cuadro de diálogo de tarea, *lParam* debe contener un identificador de un icono (HICON) que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="718ea-120">If the value of *wParam* is TDIE\_ICON\_FOOTER and the TDF\_USE\_HICON\_FOOTER flag is set on the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog, *lParam* must contain a handle to an icon (HICON) to display.</span></span>

<span data-ttu-id="718ea-121">Si \_ \_ \_ no se establecen las marcas TDF HICON Main o TDF \_ use \_ HICON \_ de  pie de página en el miembro **dwFlags** , *lParam* debe apuntar a una cadena Unicode terminada en null (PCWSTR) que contiene un identificador de recurso válido que se pasa a través de la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="718ea-121">If the TDF\_USE\_HICON\_MAIN or TDF\_USE\_HICON\_FOOTER flags are **not** set on the **dwFlags** member, *lParam* must point to a null-terminated, Unicode string (PCWSTR) that contains a valid resource identifier passed through the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="718ea-122">El icono se muestra según el valor de *wParam*: Si el valor es TDIE \_ icono \_ Main, el icono se muestra en el encabezado; si el valor es TDIE \_ Icon \_ footer, el icono se muestra en el pie de página.</span><span class="sxs-lookup"><span data-stu-id="718ea-122">The icon is displayed based on the value of *wParam*: if the value is TDIE\_ICON\_MAIN, the icon is displayed in the header; if the value is TDIE\_ICON\_FOOTER, the icon is displayed in the footer.</span></span> <span data-ttu-id="718ea-123">El recurso debe ser del módulo de recursos de la aplicación (especificado en el miembro **hInstance** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) ) o si **hInstance** es **null**, del módulo de recursos del sistema (imageres.dll).</span><span class="sxs-lookup"><span data-stu-id="718ea-123">The resource must be either from the application's resource module (specified in the **hInstance** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure), or if **hInstance** is **NULL**, from the system's resource module (imageres.dll).</span></span> <span data-ttu-id="718ea-124">Para identificar un recurso del sistema, use un identificador de sistema válido que se pase a través de la macro **MAKEINTRESOURCE** o uno de los siguientes valores predefinidos de commctrl. h:</span><span class="sxs-lookup"><span data-stu-id="718ea-124">To identify a system resource, use a valid system identifier passed through the **MAKEINTRESOURCE** macro or one of the following predefined values from commctrl.h:</span></span>



| <span data-ttu-id="718ea-125">Value</span><span class="sxs-lookup"><span data-stu-id="718ea-125">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="718ea-126">Significado</span><span class="sxs-lookup"><span data-stu-id="718ea-126">Meaning</span></span>                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <span data-ttu-id="718ea-127"><dt>**\_icono de error de TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="718ea-127"><dt>**TD\_ERROR\_ICON**</dt></span></span> </dl>                   | <span data-ttu-id="718ea-128">Un icono de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="718ea-128">A stop sign icon.</span></span><br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <span data-ttu-id="718ea-129"><dt>**\_icono de advertencia de TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="718ea-129"><dt>**TD\_WARNING\_ICON**</dt></span></span> </dl>             | <span data-ttu-id="718ea-130">Un icono de signo de exclamación.</span><span class="sxs-lookup"><span data-stu-id="718ea-130">An exclamation point icon.</span></span><br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <span data-ttu-id="718ea-131"><dt>**\_icono de información de TD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="718ea-131"><dt>**TD\_INFORMATION\_ICON**</dt></span></span> </dl> | <span data-ttu-id="718ea-132">Una letra minúscula "i" en un icono de círculo.</span><span class="sxs-lookup"><span data-stu-id="718ea-132">A lowercase letter "i" in a circle icon.</span></span><br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <span data-ttu-id="718ea-133"><dt>**icono de TD \_ Shield \_**</dt></span><span class="sxs-lookup"><span data-stu-id="718ea-133"><dt>**TD\_SHIELD\_ICON**</dt></span></span> </dl>                | <span data-ttu-id="718ea-134">Un icono de escudo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="718ea-134">A security shield icon.</span></span><br/>                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="718ea-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="718ea-135">Return value</span></span>

<span data-ttu-id="718ea-136">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="718ea-136">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="718ea-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="718ea-137">Remarks</span></span>

<span data-ttu-id="718ea-138">Se puede producir un error en el diseño del cuadro de diálogo de tarea con el icono y es posible que no se refleje en el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="718ea-138">The layout of the task dialog with the icon may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="718ea-139">Un valor devuelto de S \_ OK solo refleja que el cuadro de diálogo de tarea recibió el mensaje e intentó procesarlo.</span><span class="sxs-lookup"><span data-stu-id="718ea-139">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="718ea-140">Si se produce un error en el diseño del cuadro de diálogo de tarea, el cuadro de diálogo se cerrará y se devolverá un código **HRESULT** en la función de devolución de llamada registrada.</span><span class="sxs-lookup"><span data-stu-id="718ea-140">If the layout of the task dialog fails, the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="718ea-141">Para obtener más información sobre la sintaxis de la función de devolución de llamada, vea [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="718ea-141">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

<span data-ttu-id="718ea-142">Si el cuadro de diálogo de tarea se crea sin un pie de página (es decir, los miembros de pie de página correspondientes de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) utilizada para crear el cuadro de diálogo de tarea son **null**) y se envía este mensaje, no se agrega de forma dinámica un pie de página al cuadro de diálogo de tarea.</span><span class="sxs-lookup"><span data-stu-id="718ea-142">If the task dialog is created without a footer (that is, the appropriate footer members of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure used to create the task dialog are **NULL**) and this message is sent, a footer is not dynamically added to the task dialog.</span></span> <span data-ttu-id="718ea-143">Lo mismo se aplica al enviar este mensaje para actualizar un icono de encabezado cuando se crea un cuadro de diálogo de tarea sin un encabezado.</span><span class="sxs-lookup"><span data-stu-id="718ea-143">The same is true for sending this message to update a header icon when a task dialog is created without a header.</span></span> <span data-ttu-id="718ea-144">Para agregar un encabezado o un pie de página en tiempo de ejecución, use la funcionalidad de la [**\_ \_ Página de navegación de TDM**](tdm-navigate-page.md) .</span><span class="sxs-lookup"><span data-stu-id="718ea-144">To add a header or footer at run time, use the [**TDM\_NAVIGATE\_PAGE**](tdm-navigate-page.md) functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="718ea-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="718ea-145">Requirements</span></span>



| <span data-ttu-id="718ea-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="718ea-146">Requirement</span></span> | <span data-ttu-id="718ea-147">Value</span><span class="sxs-lookup"><span data-stu-id="718ea-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="718ea-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="718ea-148">Minimum supported client</span></span><br/> | <span data-ttu-id="718ea-149">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="718ea-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="718ea-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="718ea-150">Minimum supported server</span></span><br/> | <span data-ttu-id="718ea-151">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="718ea-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="718ea-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="718ea-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="718ea-153"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="718ea-153"><dt>Commctrl.h</dt></span></span> </dl> |



 

