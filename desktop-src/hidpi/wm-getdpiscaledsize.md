---
title: Mensaje de WM_GETDPISCALEDSIZE (Winuser. h)
description: Este mensaje indica al sistema operativo que el tamaño de la ventana se ajustará a dimensiones distintas de las predeterminadas.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- WM_GETDPISCALEDSIZE máximo de PPP del mensaje
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490750"
---
# <a name="wm_getdpiscaledsize-message"></a><span data-ttu-id="9f9cc-104">Mensaje de GETDPISCALEDSIZE de WM \_</span><span class="sxs-lookup"><span data-stu-id="9f9cc-104">WM\_GETDPISCALEDSIZE message</span></span>

<span data-ttu-id="9f9cc-105">Este mensaje indica al sistema operativo que el tamaño de la ventana se ajustará a dimensiones distintas de las predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-105">This message tells the operating system that the window will be sized to dimensions other than the default.</span></span>

<span data-ttu-id="9f9cc-106">Este mensaje se envía a ventanas de nivel superior con un [ \_ \_ contexto de reconocimiento de PPP](dpi-awareness-context.md) de por monitor V2 antes de que se envíe un mensaje de [**\_ DPICHANGED de WM**](wm-dpichanged.md) y permite que la ventana calcule su tamaño deseado para el cambio de PPP pendiente.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-106">This message is sent to top-level windows with a [DPI\_AWARENESS\_CONTEXT](dpi-awareness-context.md) of Per Monitor v2 before a [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent, and allows the window to compute its desired size for the pending DPI change.</span></span> <span data-ttu-id="9f9cc-107">Como el ajuste de escala lineal de PPP es el comportamiento predeterminado, esto solo resulta útil en escenarios donde la ventana desea escalar de forma no lineal.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-107">As linear DPI scaling is the default behavior, this is only useful in scenarios where the window wants to scale non-linearly.</span></span> <span data-ttu-id="9f9cc-108">Si la aplicación responde a este mensaje, el tamaño resultante será el rectángulo candidato enviado a **WM \_ DPICHANGED**.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-108">If the application responds to this message, the resulting size will be the candidate rectangle send to **WM\_DPICHANGED**.</span></span>

<span data-ttu-id="9f9cc-109">Use este mensaje para modificar el tamaño del rectángulo que se proporciona con [**WM \_ DPICHANGED**](wm-dpichanged.md).</span><span class="sxs-lookup"><span data-stu-id="9f9cc-109">Use this message to alter the size of the rect that is provided with [**WM\_DPICHANGED**](wm-dpichanged.md).</span></span>


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a><span data-ttu-id="9f9cc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f9cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f9cc-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f9cc-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f9cc-112">WPARAM contiene un valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-112">The WPARAM contains a DPI value.</span></span> <span data-ttu-id="9f9cc-113">El tamaño de la ventana escalada que establecería la aplicación debe calcularse como si la ventana cambiara a este valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-113">The scaled window size that the application would set needs to be computed as if the window were to switch to this DPI.</span></span>

</dd> <dt>

<span data-ttu-id="9f9cc-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f9cc-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f9cc-115">LPARAM es un puntero de in/out a una estructura de tamaño.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-115">The LPARAM is an in/out pointer to a SIZE struct.</span></span> <span data-ttu-id="9f9cc-116">El \_ valor de in \_ de lParam es el tamaño pendiente de la ventana después de un movimiento iniciado por el usuario o una llamada a [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="9f9cc-116">The \_In\_ value in the LPARAM is the pending size of the window after a user-initiated move or a call to [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="9f9cc-117">Si se cambia el tamaño de la ventana, este tamaño no es necesariamente el mismo que el tamaño actual de la ventana en el momento en que se recibe este mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-117">If the window is being resized, this size is not necessarily the same as the window's current size at the time this message is received.</span></span>

<span data-ttu-id="9f9cc-118">El \_ \_ valor out en lParam debe escribirse en la aplicación para especificar el tamaño de ventana escalado deseado correspondiente al valor de PPP proporcionado en el wParam.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-118">The \_Out\_ value in the LPARAM should be written to by the application to specify the desired scaled window size corresponding to the provided DPI value in the WPARAM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f9cc-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f9cc-119">Return value</span></span>

<span data-ttu-id="9f9cc-120">La función devuelve un BOOLEANO.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-120">The function returns a BOOL.</span></span> <span data-ttu-id="9f9cc-121">Si devuelve TRUE, indica que se ha calculado un nuevo tamaño.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-121">Returning TRUE indicates that a new size has been computed.</span></span> <span data-ttu-id="9f9cc-122">Si devuelve FALSE, indica que el mensaje no se controlará y el ajuste de escala lineal de PPP se aplicará a la ventana.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-122">Returning FALSE indicates that the message will not be handled, and the default linear DPI scaling will apply to the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f9cc-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f9cc-123">Remarks</span></span>

<span data-ttu-id="9f9cc-124">Este mensaje solo se envía a las ventanas de nivel superior que tienen un contexto de reconocimiento de PPP de por monitor V2.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-124">This message is only sent to top-level windows which have a DPI awareness context of Per Monitor v2.</span></span>

<span data-ttu-id="9f9cc-125">Este evento es necesario para facilitar el escalado no lineal estable y garantiza que la posición de Windows permanezca constante en relación con el cursor y al avanzar y retroceder por los monitores.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-125">This event is necessary to facilitate graceful non-linear scaling, and ensures that the windows's position remains constant in relationship to the cursor and when moving back and forth across monitors.</span></span>

<span data-ttu-id="9f9cc-126">No hay ningún control predeterminado específico de este mensaje en [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="9f9cc-126">There is no specific default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="9f9cc-127">En cuanto a todos los mensajes que no controla explícitamente, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) devolverá cero para este mensaje.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-127">As for all messages it does not explicitly handle, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will return zero for this message.</span></span> <span data-ttu-id="9f9cc-128">Como se indicó anteriormente, este valor devuelto indica al sistema que use el comportamiento lineal predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9f9cc-128">As noted above, this return tells the system to use the default linear behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f9cc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f9cc-129">Requirements</span></span>



| <span data-ttu-id="9f9cc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f9cc-130">Requirement</span></span> | <span data-ttu-id="9f9cc-131">Value</span><span class="sxs-lookup"><span data-stu-id="9f9cc-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9f9cc-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f9cc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9f9cc-133">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f9cc-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9f9cc-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f9cc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9f9cc-135">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f9cc-135">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9f9cc-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f9cc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f9cc-137"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f9cc-137"><dt>Winuser.h</dt></span></span> </dl> |



 

