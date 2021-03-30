---
description: Se envía cuando el sistema pide a una ventana qué gestos del sistema desea recibir.
ms.assetid: 5b747b3c-3b77-4913-932f-182114d1f674
title: Mensaje de WM_TABLET_QUERYSYSTEMGESTURESTATUS (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 395196f963cae9b8d18697276e546f1eba05b245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907908"
---
# <a name="wm_tablet_querysystemgesturestatus-message"></a><span data-ttu-id="3692c-103">\_Mensaje de QUERYSYSTEMGESTURESTATUS de Tablet PC de WM \_</span><span class="sxs-lookup"><span data-stu-id="3692c-103">WM\_TABLET\_QUERYSYSTEMGESTURESTATUS message</span></span>

<span data-ttu-id="3692c-104">Se envía cuando el sistema pide a una ventana qué gestos del sistema desea recibir.</span><span class="sxs-lookup"><span data-stu-id="3692c-104">Sent when the system asks a window which system gestures it would like to receive.</span></span>


```C++
#define WM_TABLET_DEFBASE                    0x02C0
#define WM_TABLET_QUERYSYSTEMGESTURESTATUS   (WM_TABLET_DEFBASE + 12)       
```



## <a name="parameters"></a><span data-ttu-id="3692c-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3692c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3692c-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3692c-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3692c-107">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3692c-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3692c-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3692c-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3692c-109">Un valor de punto que representa las coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="3692c-109">A point value that represents the screen coordinates.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3692c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3692c-110">Remarks</span></span>

<span data-ttu-id="3692c-111">Al controlar este mensaje, puede deshabilitar los gestos de forma dinámica para las regiones de una ventana.</span><span class="sxs-lookup"><span data-stu-id="3692c-111">By handling this message, you can dynamically disable flicks for regions of a window.</span></span>

> [!Note]  
> <span data-ttu-id="3692c-112">*LParam* se puede convertir en coordenadas x e y mediante las `GET_X_LPARAM` `GET_Y_LPARAM` macros y.</span><span class="sxs-lookup"><span data-stu-id="3692c-112">The *lParam* can be converted to x-coordinates and y-coordinates by using the `GET_X_LPARAM` and `GET_Y_LPARAM` macros.</span></span>

 

<span data-ttu-id="3692c-113">De forma predeterminada, la ventana recibirá todos los eventos de gestos del sistema.</span><span class="sxs-lookup"><span data-stu-id="3692c-113">By default, your window will receive all system gesture events.</span></span> <span data-ttu-id="3692c-114">Puede elegir los eventos que desea que reciba la ventana y los eventos que desea deshabilitar al responder al mensaje de **\_ \_ QUERYSYSTEMGESTURESTATUS** de la tableta de WM en el **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="3692c-114">You can choose which events you would like your window to receive and which events you would like disabled by responding to the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message in your **WndProc**.</span></span> <span data-ttu-id="3692c-115">El mensaje de **\_ \_ QUERYSYSTEMGESTURESTATUS** de la tableta de WM se define en tpcshrd. h.</span><span class="sxs-lookup"><span data-stu-id="3692c-115">The **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message is defined in tpcshrd.h.</span></span> <span data-ttu-id="3692c-116">Los valores para habilitar y deshabilitar los gestos del sistema de la tableta del sistema también se definen en tpcshrd. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3692c-116">The values to enable and disable system tablet system gestures are also defined in tpcshrd.h as follows:</span></span>

``` syntax
#define TABLET_DISABLE_PRESSANDHOLD        0x00000001
#define TABLET_DISABLE_PENTAPFEEDBACK      0x00000008
#define TABLET_DISABLE_PENBARRELFEEDBACK   0x00000010
#define TABLET_DISABLE_TOUCHUIFORCEON      0x00000100
#define TABLET_DISABLE_TOUCHUIFORCEOFF     0x00000200
#define TABLET_DISABLE_TOUCHSWITCH         0x00008000
#define TABLET_DISABLE_FLICKS              0x00010000
#define TABLET_ENABLE_FLICKSONCONTEXT      0x00020000
#define TABLET_ENABLE_FLICKLEARNINGMODE    0x00040000
#define TABLET_DISABLE_SMOOTHSCROLLING     0x00080000
#define TABLET_DISABLE_FLICKFALLBACKKEYS   0x00100000
#define TABLET_ENABLE_MULTITOUCHDATA       0x01000000
```

> [!Note]
>
> <span data-ttu-id="3692c-117">Al deshabilitar la función de mantener presionado se mejora la capacidad de respuesta de los clics del mouse porque esta funcionalidad crea un tiempo de espera para distinguir entre las dos operaciones.</span><span class="sxs-lookup"><span data-stu-id="3692c-117">Disabling press and hold will improve responsiveness for mouse clicks because this functionality creates a wait time to distinguish between the two operations.</span></span>

 

<span data-ttu-id="3692c-118">Tenga precaución al controlar el mensaje de **\_ \_ QUERYSYSTEMGESTURESTATUS** de la tableta de WM.</span><span class="sxs-lookup"><span data-stu-id="3692c-118">Use caution when handling the **WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** message.</span></span> <span data-ttu-id="3692c-119">**WM \_ TABLET \_ QUERYSYSTEMGESTURESTATUS** se pasa mediante la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="3692c-119">**WM\_TABLET\_QUERYSYSTEMGESTURESTATUS** is passed using the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span> <span data-ttu-id="3692c-120">Si llama a métodos en una interfaz COM, ese objeto debe estar dentro del mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="3692c-120">If you call methods on a COM interface, that object must be within the same process.</span></span> <span data-ttu-id="3692c-121">De lo contrario, COM produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="3692c-121">If not, COM throws an exception.</span></span>

## <a name="examples"></a><span data-ttu-id="3692c-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3692c-122">Examples</span></span>

<span data-ttu-id="3692c-123">En el ejemplo siguiente se muestra cómo deshabilitar los gestos para una región mediante WM \_ Tablet \_ QUERYSYSTEMGESTURESTATUS.</span><span class="sxs-lookup"><span data-stu-id="3692c-123">The following example shows how to disable flicks for a region using WM\_TABLET\_QUERYSYSTEMGESTURESTATUS.</span></span>


```C++
#include <windowsx.h>        

(...)        
        
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    case WM_TABLET_QUERYSYSTEMGESTURESTATUS:
        int x = GET_X_LPARAM(lParam);
        int y = GET_Y_LPARAM(lParam);
        if (x < xThreashold && y < yThreshold){
            // no flicks in the region specified by the threashold
            return TABLET_DISABLE_FLICKS;
        }
        // flicks will happen otherwise
        return 0;
}        
        
```



<span data-ttu-id="3692c-124">En el ejemplo siguiente se muestra cómo deshabilitar varias características de gestos para una ventana completa.</span><span class="sxs-lookup"><span data-stu-id="3692c-124">The following example shows how to disable various flicks features for an entire window.</span></span>


```C++
const DWORD dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
        
void SetTabletpenserviceProperties(HWND hWnd){
    ATOM atom = ::GlobalAddAtom(MICROSOFT_TABLETPENSERVICE_PROPERTY);    
    ::SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
    ::GlobalDeleteAtom(atom);
}        
        
```



## <a name="requirements"></a><span data-ttu-id="3692c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3692c-125">Requirements</span></span>



| <span data-ttu-id="3692c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3692c-126">Requirement</span></span> | <span data-ttu-id="3692c-127">Value</span><span class="sxs-lookup"><span data-stu-id="3692c-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3692c-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3692c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3692c-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3692c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3692c-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3692c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3692c-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3692c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3692c-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3692c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3692c-133"><dt>Tpcshrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="3692c-133"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
