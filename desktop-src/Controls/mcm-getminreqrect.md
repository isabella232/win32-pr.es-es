---
title: Mensaje de MCM_GETMINREQRECT (commctrl. h)
description: Recupera el tamaño mínimo necesario para mostrar un mes completo en un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetMinReqRect.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- MCM_GETMINREQRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489964"
---
# <a name="mcm_getminreqrect-message"></a><span data-ttu-id="c6b05-105">Mensaje de MCM \_ GETMINREQRECT</span><span class="sxs-lookup"><span data-stu-id="c6b05-105">MCM\_GETMINREQRECT message</span></span>

<span data-ttu-id="c6b05-106">Recupera el tamaño mínimo necesario para mostrar un mes completo en un control de calendario mensual.</span><span class="sxs-lookup"><span data-stu-id="c6b05-106">Retrieves the minimum size required to display a full month in a month calendar control.</span></span> <span data-ttu-id="c6b05-107">Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) .</span><span class="sxs-lookup"><span data-stu-id="c6b05-107">You can send this message explicitly or by using the [**MonthCal\_GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6b05-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6b05-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6b05-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6b05-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c6b05-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c6b05-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c6b05-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6b05-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6b05-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibirá información del rectángulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="c6b05-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive bounding rectangle information.</span></span> <span data-ttu-id="c6b05-113">Este parámetro debe ser una dirección válida y no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c6b05-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6b05-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6b05-114">Return value</span></span>

<span data-ttu-id="c6b05-115">Devuelve un valor distinto de cero y *lParam* recibe la información de límite aplicable si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c6b05-115">Returns nonzero and *lParam* receives the applicable bounding information if successful.</span></span> <span data-ttu-id="c6b05-116">De lo contrario, el mensaje devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="c6b05-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6b05-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6b05-117">Remarks</span></span>

<span data-ttu-id="c6b05-118">El tamaño mínimo de ventana necesario para un control de calendario mensual depende de la fuente, los estilos de control, las métricas del sistema y la configuración regional seleccionados actualmente.</span><span class="sxs-lookup"><span data-stu-id="c6b05-118">The minimum required window size for a month calendar control depends on the currently selected font, control styles, system metrics, and regional settings.</span></span> <span data-ttu-id="c6b05-119">Cuando una aplicación cambia todo lo que afecta al tamaño mínimo de la ventana o procesa un mensaje de [**\_ SETTINGCHANGE de WM**](/windows/desktop/winmsg/wm-settingchange) , debe enviar **MCM \_ GETMINREQRECT** para determinar el nuevo tamaño mínimo.</span><span class="sxs-lookup"><span data-stu-id="c6b05-119">When an application changes anything that affects the minimum window size, or processes a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message, it should send **MCM\_GETMINREQRECT** to determine the new minimum size.</span></span>

> [!Note]  
> <span data-ttu-id="c6b05-120">El rectángulo devuelto por **MCM \_ GETMINREQRECT** no incluye el ancho de la cadena "Today", si está presente.</span><span class="sxs-lookup"><span data-stu-id="c6b05-120">The rectangle returned by **MCM\_GETMINREQRECT** does not include the width of the "Today" string, if it is present.</span></span> <span data-ttu-id="c6b05-121">Si no se establece el estilo [**MCS \_ noactual**](month-calendar-control-styles.md) , la aplicación también debe recuperar el rectángulo que define el ancho de la cadena "Today" mediante el envío de un mensaje [**\_ GETMAXTODAYWIDTH de MCM**](mcm-getmaxtodaywidth.md) .</span><span class="sxs-lookup"><span data-stu-id="c6b05-121">If the [**MCS\_NOTODAY**](month-calendar-control-styles.md) style is not set, your application should also retrieve the rectangle that defines the "Today" string width by sending a [**MCM\_GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) message.</span></span> <span data-ttu-id="c6b05-122">Utilice el mayor de los dos rectángulos para asegurarse de que la cadena "Today" no se recorte.</span><span class="sxs-lookup"><span data-stu-id="c6b05-122">Use the larger of the two rectangles to ensure that the "Today" string is not clipped.</span></span>

 

<span data-ttu-id="c6b05-123">Los miembros **superior** e **izquierdo** de la estructura a la que apunta *lParam* siempre serán cero.</span><span class="sxs-lookup"><span data-stu-id="c6b05-123">The **top** and **left** members of the structure pointed to by *lParam* will always be zero.</span></span> <span data-ttu-id="c6b05-124">Los miembros **derecho** e **inferior** representan el mínimo de *CX* y *CY* necesarios para el control.</span><span class="sxs-lookup"><span data-stu-id="c6b05-124">The **right** and **bottom** members represent the minimum *cx* and *cy* required for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b05-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6b05-125">Requirements</span></span>



| <span data-ttu-id="c6b05-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6b05-126">Requirement</span></span> | <span data-ttu-id="c6b05-127">Value</span><span class="sxs-lookup"><span data-stu-id="c6b05-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b05-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6b05-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b05-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c6b05-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6b05-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6b05-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b05-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6b05-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6b05-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6b05-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6b05-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6b05-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

