---
description: Indica a una ventana de colocación de la imagen que actualice con la nueva información de DROPDESCRIPTION.
title: Mensaje DDWM_UPDATEWINDOW
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bff0e007c735fcf202aaf16cf304eb4ff5358f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984315"
---
# <a name="ddwm_updatewindow-message"></a><span data-ttu-id="18e78-103">DDWM \_ UPDATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="18e78-103">DDWM\_UPDATEWINDOW message</span></span>

<span data-ttu-id="18e78-104">Indica a una ventana de colocación de la imagen que actualice con la nueva información de [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) .</span><span class="sxs-lookup"><span data-stu-id="18e78-104">Instructs a drop image window to update using new [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) information.</span></span>

## <a name="parameters"></a><span data-ttu-id="18e78-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="18e78-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18e78-106">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18e78-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18e78-107">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="18e78-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="18e78-108">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="18e78-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18e78-109">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="18e78-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18e78-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18e78-110">Remarks</span></span>

<span data-ttu-id="18e78-111">DDWM \_ UPDATEWINDOW se define como usuario de WM \_ + 3.</span><span class="sxs-lookup"><span data-stu-id="18e78-111">DDWM\_UPDATEWINDOW is defined as WM\_USER+3.</span></span>

<span data-ttu-id="18e78-112">Cuando cambia el estado de una operación de colocar, por ejemplo, en respuesta a una tecla modificadora,[**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) devuelve un nuevo valor de [**DROPEFFECT**](../com/dropeffect-constants.md) (este valor de **DROPEFFECT** también se puede recibir a través de [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span><span class="sxs-lookup"><span data-stu-id="18e78-112">When the state of a drop operation changes—such as in response to a modifier key—[**IDropTarget::DragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) returns a new [**DROPEFFECT**](../com/dropeffect-constants.md) value (this **DROPEFFECT** value can also be received through [**IDropSource::GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span></span> <span data-ttu-id="18e78-113">En respuesta, la aplicación actualiza la estructura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) del destino de colocación con un nuevo valor [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) que indica la decoración que se va a aplicar al visual de la ventana de arrastre. por ejemplo, indica que el archivo se está copiando en lugar de moverse o que el objeto no se puede quitar a esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="18e78-113">In response, the application updates the drop target's [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) structure with a new [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) value that indicates the decoration to be applied to the drag window's visual; for instance, an indication that the file is being copied rather than moved or that the object cannot be dropped to that location.</span></span> <span data-ttu-id="18e78-114">Sin embargo, los objetos visuales no se actualizan hasta que el objeto recibe un mensaje **\_ UPDATEWINDOW de DDWM** .</span><span class="sxs-lookup"><span data-stu-id="18e78-114">However, the visuals are not updated until the object receives a **DDWM\_UPDATEWINDOW** message.</span></span>

<span data-ttu-id="18e78-115">El formato del portapapeles de [DragWindow](clipboard.md) proporciona el **hWnd** de la ventana de arrastre del destinatario al remitente del mensaje de **\_ UPDATEWINDOW de DDWM** .</span><span class="sxs-lookup"><span data-stu-id="18e78-115">The [DragWindow](clipboard.md) clipboard format provides the **HWND** of the recipient drag window to the sender of the **DDWM\_UPDATEWINDOW** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="18e78-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18e78-116">Requirements</span></span>



| <span data-ttu-id="18e78-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="18e78-117">Requirement</span></span> | <span data-ttu-id="18e78-118">Value</span><span class="sxs-lookup"><span data-stu-id="18e78-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="18e78-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18e78-119">Minimum supported client</span></span><br/> | <span data-ttu-id="18e78-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="18e78-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="18e78-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18e78-121">Minimum supported server</span></span><br/> | <span data-ttu-id="18e78-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="18e78-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
