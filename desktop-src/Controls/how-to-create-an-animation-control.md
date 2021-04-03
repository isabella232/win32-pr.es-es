---
title: Cómo crear un control Animation
description: En este tema se muestra cómo crear un control de animación.
ms.assetid: 5852B636-F3D0-47A4-82F6-8BE570013E1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ff190617996e42e6580b82311fb51f4248000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075344"
---
# <a name="how-to-create-an-animation-control"></a><span data-ttu-id="b0893-103">Cómo crear un control Animation</span><span class="sxs-lookup"><span data-stu-id="b0893-103">How to Create an Animation Control</span></span>

<span data-ttu-id="b0893-104">En este tema se muestra cómo crear un control de animación.</span><span class="sxs-lookup"><span data-stu-id="b0893-104">This topic demonstrates how to create an animation control.</span></span> <span data-ttu-id="b0893-105">El ejemplo de código de C++ que lo acompaña crea un control de animación en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b0893-105">The accompanying C++ code example creates an animation control in a dialog box.</span></span> <span data-ttu-id="b0893-106">Coloca el control Animation debajo de un control especificado y establece las dimensiones del control Animation basándose en las dimensiones de un marco en el Audio-Video clip intercalado (AVI).</span><span class="sxs-lookup"><span data-stu-id="b0893-106">It positions the animation control below a specified control, and sets the dimensions of the animation control based on the dimensions of a frame in the Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b0893-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="b0893-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b0893-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="b0893-108">Technologies</span></span>

-   [<span data-ttu-id="b0893-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="b0893-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b0893-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b0893-110">Prerequisites</span></span>

-   <span data-ttu-id="b0893-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="b0893-111">C/C++</span></span>
-   <span data-ttu-id="b0893-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="b0893-112">Windows User Interface Programming</span></span>
-   <span data-ttu-id="b0893-113">Archivos AVI</span><span class="sxs-lookup"><span data-stu-id="b0893-113">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="b0893-114">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="b0893-114">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-animation-control"></a><span data-ttu-id="b0893-115">Paso 1: crear una instancia del control Animation.</span><span class="sxs-lookup"><span data-stu-id="b0893-115">Step 1: Create an instance of the animation control.</span></span>

<span data-ttu-id="b0893-116">Utilice [**Animate \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro para crear una instancia del control Animation.</span><span class="sxs-lookup"><span data-stu-id="b0893-116">Use the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro to create an instance of the animation control.</span></span>


```C++
// IDC_ANIMATE - identifier of the animation control. 
// hwndDlg - handle to the dialog box.
RECT rc;
hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
    WS_BORDER | WS_CHILD, g_hinst); 
```



### <a name="step-2-position-the-animation-control"></a><span data-ttu-id="b0893-117">Paso 2: colocar el control de animación.</span><span class="sxs-lookup"><span data-stu-id="b0893-117">Step 2: Position the animation control.</span></span>

<span data-ttu-id="b0893-118">Obtiene las coordenadas de pantalla del botón de control especificado.</span><span class="sxs-lookup"><span data-stu-id="b0893-118">Get the screen coordinates of the specified control button.</span></span>


```C++
// nIDCtl - identifier of the control below which the animation control is to be positioned.
GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 
```



<span data-ttu-id="b0893-119">Convierte las coordenadas de la esquina inferior izquierda en coordenadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="b0893-119">Convert the coordinates of the lower-left corner to client coordinates.</span></span>


```C++
POINT pt;
pt.x = rc.left; 
pt.y = rc.bottom; 
ScreenToClient(hwndDlg, &pt); 
```



<span data-ttu-id="b0893-120">Coloque el control de animación debajo del botón de control especificado.</span><span class="sxs-lookup"><span data-stu-id="b0893-120">Position the animation control below the specified control button.</span></span>


```C++
// CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
    CX_FRAME, CY_FRAME, 
    SWP_NOZORDER | SWP_DRAWFRAME);
```



### <a name="step-3-open-the-avi-clip"></a><span data-ttu-id="b0893-121">Paso 3: Abra el clip AVI.</span><span class="sxs-lookup"><span data-stu-id="b0893-121">Step 3: Open the AVI clip.</span></span>

<span data-ttu-id="b0893-122">Llame a la macro [**animada \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) para abrir el clip AVI y mostrar el primer fotograma en el control Animation.</span><span class="sxs-lookup"><span data-stu-id="b0893-122">Call the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) macro to open the AVI clip and display the first frame in the animation control.</span></span> <span data-ttu-id="b0893-123">Llame a la función **ShowWindow** para que el control de animación sea visible.</span><span class="sxs-lookup"><span data-stu-id="b0893-123">Call the **ShowWindow** function to make the animation control visible.</span></span>


```C++
Animate_Open(hwndAnim, "SEARCH.AVI"); 
ShowWindow(hwndAnim, SW_SHOW); 
```



## <a name="complete-example"></a><span data-ttu-id="b0893-124">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="b0893-124">Complete example</span></span>


```C++
// CreateAnimationCtrl - creates an animation control, positions it 
//                       below the specified control in a dialog box, 
//                       and opens the AVI clip for the animation control. 
// Returns the handle to the animation control. 
// hwndDlg             - handle to the dialog box. 
// nIDCtl              - identifier of the control below which the animation control 
//                       is to be positioned. 
// 
// Constants 
//     IDC_ANIMATE - identifier of the animation control. 
//     CX_FRAME, CY_FRAME - width and height of the frames 
//     in the AVI clip. 

HWND CreateAnimationCtrl(HWND hwndDlg, int nIDCtl) 
{ 
    HWND hwndAnim = NULL;    
    
    // Create the animation control.
    // IDC_ANIMATE - identifier of the animation control. 
    // hwndDlg - handle to the dialog box.
    RECT rc;
    hwndAnim = Animate_Create(hwndDlg, IDC_ANIMATE, 
        WS_BORDER | WS_CHILD, g_hinst); 

    // Get the screen coordinates of the specified control button.
    // nIDCtl - identifier of the control below which the animation control is to be positioned.
    GetWindowRect(GetDlgItem(hwndDlg, nIDCtl), &rc); 

    // Convert the coordinates of the lower-left corner to 
    // client coordinates.
    POINT pt;
    pt.x = rc.left; 
    pt.y = rc.bottom; 
    ScreenToClient(hwndDlg, &pt); 

    // Position the animation control below the Stop button.
    // CX_FRAME, CY_FRAME - width and height of the frames in the AVI clip.      
    SetWindowPos(hwndAnim, 0, pt.x, pt.y + 20, 
        CX_FRAME, CY_FRAME, 
        SWP_NOZORDER | SWP_DRAWFRAME);

    // Open the AVI clip, and show the animation control.
    Animate_Open(hwndAnim, "SEARCH.AVI"); 
    ShowWindow(hwndAnim, SW_SHOW); 

    return hwndAnim; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="b0893-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b0893-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0893-126">Acerca de los controles de animación</span><span class="sxs-lookup"><span data-stu-id="b0893-126">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="b0893-127">Referencia de control de animación</span><span class="sxs-lookup"><span data-stu-id="b0893-127">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b0893-128">Usar controles de animación</span><span class="sxs-lookup"><span data-stu-id="b0893-128">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="b0893-129">Animación</span><span class="sxs-lookup"><span data-stu-id="b0893-129">Animation</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




