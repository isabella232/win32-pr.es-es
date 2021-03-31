---
title: Mensaje de HDM_LAYOUT (commctrl. h)
description: Recupera información utilizada para establecer el tamaño y la posición del control de encabezado dentro del rectángulo de destino de la ventana primaria. Puede enviar este mensaje explícitamente o utilizar la macro de diseño de encabezado \_ .
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- HDM_LAYOUT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70fc46dee52f52862136dbe583db9f6d7a0e13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079402"
---
# <a name="hdm_layout-message"></a><span data-ttu-id="945b4-105">Mensaje de diseño de HDM \_</span><span class="sxs-lookup"><span data-stu-id="945b4-105">HDM\_LAYOUT message</span></span>

<span data-ttu-id="945b4-106">Recupera información utilizada para establecer el tamaño y la posición del control de encabezado dentro del rectángulo de destino de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="945b4-106">Retrieves information used to set the size and position of the header control within the target rectangle of the parent window.</span></span> <span data-ttu-id="945b4-107">Puede enviar este mensaje explícitamente o utilizar la macro de [**\_ diseño de encabezado**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) .</span><span class="sxs-lookup"><span data-stu-id="945b4-107">You can send this message explicitly or use the [**Header\_Layout**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="945b4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="945b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="945b4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="945b4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="945b4-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="945b4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="945b4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="945b4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="945b4-112">Puntero a una estructura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) .</span><span class="sxs-lookup"><span data-stu-id="945b4-112">A pointer to an [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) structure.</span></span> <span data-ttu-id="945b4-113">El miembro **PRC** especifica las coordenadas de un rectángulo y el miembro **pwpos** recibe el tamaño y la posición del control de encabezado dentro del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="945b4-113">The **prc** member specifies the coordinates of a rectangle, and the **pwpos** member receives the size and position for the header control within the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="945b4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="945b4-114">Return value</span></span>

<span data-ttu-id="945b4-115">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="945b4-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="945b4-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="945b4-116">Remarks</span></span>

<span data-ttu-id="945b4-117">El miembro **pwpos** de la estructura *lParam* recibe los valores de tamaño y posición adecuados para colocar el control a lo largo de la parte superior del rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="945b4-117">The **pwpos** member of the *lParam* structure receives size and position values appropriate for positioning the control along the top of the specified rectangle.</span></span> <span data-ttu-id="945b4-118">El valor de alto es la suma de los altos de los bordes horizontales del control y el alto medio de los caracteres de la fuente actualmente seleccionada en el contexto del dispositivo del control.</span><span class="sxs-lookup"><span data-stu-id="945b4-118">The height value is the sum of the heights of the control's horizontal borders and the average height of characters in the font currently selected into the control's device context.</span></span>

<span data-ttu-id="945b4-119">Para usar **el \_ diseño de HDM** para establecer el tamaño y la posición iniciales de un control de encabezado, establezca el estado de visibilidad inicial del control para que esté oculto.</span><span class="sxs-lookup"><span data-stu-id="945b4-119">To use **HDM\_LAYOUT** to set the initial size and position of a header control, set the initial visibility state of the control so that it is hidden.</span></span> <span data-ttu-id="945b4-120">Después de enviar el **\_ diseño de HDM** para recuperar los valores de tamaño y posición, utilice la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para establecer el nuevo tamaño, la posición y el estado de visibilidad.</span><span class="sxs-lookup"><span data-stu-id="945b4-120">After sending **HDM\_LAYOUT** to retrieve the size and position values, use the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to set the new size, position, and visibility state.</span></span>

## <a name="requirements"></a><span data-ttu-id="945b4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="945b4-121">Requirements</span></span>



| <span data-ttu-id="945b4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="945b4-122">Requirement</span></span> | <span data-ttu-id="945b4-123">Value</span><span class="sxs-lookup"><span data-stu-id="945b4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="945b4-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="945b4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="945b4-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="945b4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="945b4-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="945b4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="945b4-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="945b4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="945b4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="945b4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="945b4-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="945b4-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

