---
title: Mensaje de TDM_NAVIGATE_PAGE (commctrl. h)
description: Vuelve a crear un cuadro de diálogo de tarea con contenido nuevo, simulando la funcionalidad de un asistente de varias páginas.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- TDM_NAVIGATE_PAGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56fc86e0e4fe457a43e035ed5d568e91303c7fcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997021"
---
# <a name="tdm_navigate_page-message"></a><span data-ttu-id="65a78-104">Mensaje de página de \_ navegación de TDM \_</span><span class="sxs-lookup"><span data-stu-id="65a78-104">TDM\_NAVIGATE\_PAGE message</span></span>

<span data-ttu-id="65a78-105">Vuelve a crear un cuadro de diálogo de tarea con contenido nuevo, simulando la funcionalidad de un asistente de varias páginas.</span><span class="sxs-lookup"><span data-stu-id="65a78-105">Recreates a task dialog with new contents, simulating the functionality of a multi-page wizard.</span></span>

## <a name="parameters"></a><span data-ttu-id="65a78-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65a78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65a78-107">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65a78-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a78-108">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="65a78-108">Not used.</span></span> <span data-ttu-id="65a78-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="65a78-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="65a78-110">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65a78-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a78-111">Puntero a una estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que describe el cuadro de diálogo de tarea que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="65a78-111">A pointer to a [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that describes the task dialog to create.</span></span> <span data-ttu-id="65a78-112">La aplicación que realiza la llamada debe asignar esta estructura y establecer sus miembros.</span><span class="sxs-lookup"><span data-stu-id="65a78-112">The calling application must allocate this structure and set its members.</span></span> <span data-ttu-id="65a78-113">Los valores de los miembros varían en función del tipo de página al que navega el usuario.</span><span class="sxs-lookup"><span data-stu-id="65a78-113">The values of the members vary depending on the kind of page the user navigates to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65a78-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65a78-114">Return value</span></span>

<span data-ttu-id="65a78-115">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="65a78-115">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="65a78-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65a78-116">Remarks</span></span>

<span data-ttu-id="65a78-117">Para iniciar un cuadro de diálogo de tarea del asistente, use la función [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="65a78-117">To launch a wizard task dialog, use the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="65a78-118">Cuando el usuario navega con el asistente, envía este mensaje al cuadro de diálogo de la tarea para mostrar la página siguiente.</span><span class="sxs-lookup"><span data-stu-id="65a78-118">As the user navigates using the wizard, send this message to the task dialog to display the next page.</span></span> <span data-ttu-id="65a78-119">Se crea un nuevo cuadro de diálogo de tarea (se parece a una nueva página) con los elementos especificados en la estructura a la que apunta *lParam*.</span><span class="sxs-lookup"><span data-stu-id="65a78-119">A new task dialog (looks like a new page) is created with the elements specified in the structure pointed to by *lParam*.</span></span> <span data-ttu-id="65a78-120">En el momento de la creación, se destruye y se reconstruye todo el contenido del marco del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="65a78-120">At creation, the entire contents of the dialog frame are destroyed and reconstructed.</span></span> <span data-ttu-id="65a78-121">Como resultado, se pierde toda la información de estado mantenida por los controles (por ejemplo, una barra de progreso, un botón Expando o una casilla de verificación) en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="65a78-121">As a result, any state information held by controls (for example, a progress bar, expando button, or verification checkbox) in the dialog is lost.</span></span>

<span data-ttu-id="65a78-122">Se puede producir un error en el diseño del cuadro de diálogo de tarea y es posible que no se refleje en el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="65a78-122">The layout of the task dialog may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="65a78-123">Un valor devuelto de S \_ OK solo refleja que el cuadro de diálogo de tarea recibió el mensaje e intentó procesarlo.</span><span class="sxs-lookup"><span data-stu-id="65a78-123">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="65a78-124">Si se produce un error en el diseño del cuadro de diálogo de tarea (no se puede mostrar el cuadro de diálogo de tarea), el cuadro de diálogo se cerrará y se devolverá un código **HRESULT** en la función de devolución de llamada registrada.</span><span class="sxs-lookup"><span data-stu-id="65a78-124">If the layout of the task dialog fails (the task dialog cannot be displayed), the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="65a78-125">Para obtener más información sobre la sintaxis de la función de devolución de llamada, vea [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="65a78-125">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

## <a name="requirements"></a><span data-ttu-id="65a78-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65a78-126">Requirements</span></span>



| <span data-ttu-id="65a78-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="65a78-127">Requirement</span></span> | <span data-ttu-id="65a78-128">Value</span><span class="sxs-lookup"><span data-stu-id="65a78-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65a78-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65a78-129">Minimum supported client</span></span><br/> | <span data-ttu-id="65a78-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="65a78-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65a78-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65a78-131">Minimum supported server</span></span><br/> | <span data-ttu-id="65a78-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="65a78-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65a78-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65a78-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="65a78-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="65a78-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

