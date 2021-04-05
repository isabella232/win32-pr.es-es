---
title: Cómo usar los controles de buscapersonas
description: En esta sección se describe cómo implementar el control de paginación en la aplicación.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bfff0c8d8097c4b0e861506bb73f55467b711
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078452"
---
# <a name="how-to-use-pager-controls"></a><span data-ttu-id="47204-103">Cómo usar los controles de buscapersonas</span><span class="sxs-lookup"><span data-stu-id="47204-103">How to Use Pager Controls</span></span>

<span data-ttu-id="47204-104">En esta sección se describe cómo implementar el control de paginación en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="47204-104">This section describes how to implement the pager control in your application.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="47204-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="47204-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="47204-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="47204-106">Technologies</span></span>

-   [<span data-ttu-id="47204-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="47204-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="47204-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="47204-108">Prerequisites</span></span>

-   <span data-ttu-id="47204-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="47204-109">C/C++</span></span>
-   <span data-ttu-id="47204-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="47204-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="47204-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="47204-111">Instructions</span></span>

### <a name="initialize-a-pager-control"></a><span data-ttu-id="47204-112">Inicializar un control de paginación</span><span class="sxs-lookup"><span data-stu-id="47204-112">Initialize a Pager Control</span></span>

<span data-ttu-id="47204-113">Para usar el control de paginación, debe llamar a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con la \_ \_ marca de clase PAGESCROLLER de ICC establecida en el miembro **dwICC** de la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="47204-113">To use the pager control, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function with the ICC\_PAGESCROLLER\_CLASS flag set in the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure.</span></span>

### <a name="create-a-pager-control"></a><span data-ttu-id="47204-114">Crear un control de paginación</span><span class="sxs-lookup"><span data-stu-id="47204-114">Create a Pager Control</span></span>

<span data-ttu-id="47204-115">Use la API [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de paginación.</span><span class="sxs-lookup"><span data-stu-id="47204-115">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) API to create a pager control.</span></span> <span data-ttu-id="47204-116">El nombre de clase del control es [**WC \_ PAGESCROLLER**](common-control-window-classes.md), que se define en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="47204-116">The class name for the control is [**WC\_PAGESCROLLER**](common-control-window-classes.md), which is defined in Commctrl.h.</span></span> <span data-ttu-id="47204-117">El estilo [**págs \_ horizontal**](pager-control-styles.md) se usa para crear un buscapersonas horizontal y el estilo [**págs \_ Vert**](pager-control-styles.md) se usa para crear un buscapersonas vertical.</span><span class="sxs-lookup"><span data-stu-id="47204-117">The [**PGS\_HORZ**](pager-control-styles.md) style is used to create a horizontal pager, and the [**PGS\_VERT**](pager-control-styles.md) style is used to create a vertical pager.</span></span> <span data-ttu-id="47204-118">Dado que se trata de un control secundario, también debe usarse el estilo [**WS \_ Child**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="47204-118">Because this is a child control, the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style should also be used.</span></span>

<span data-ttu-id="47204-119">Una vez creado el control de paginación, lo más probable es que desee asignarle una ventana contenida.</span><span class="sxs-lookup"><span data-stu-id="47204-119">After the pager control is created, you will most likely want to assign a contained window to it.</span></span> <span data-ttu-id="47204-120">Si la ventana contenida es una ventana secundaria, debe convertir la ventana secundaria en un elemento secundario del control de paginación para que el tamaño y la posición se calculen correctamente.</span><span class="sxs-lookup"><span data-stu-id="47204-120">If the contained window is a child window, you should make the child window a child of the pager control so that the size and position will be calculated correctly.</span></span> <span data-ttu-id="47204-121">A continuación, asigne la ventana al control de paginación con el mensaje [**PGM \_ SETCHILD**](pgm-setchild.md) .</span><span class="sxs-lookup"><span data-stu-id="47204-121">You then assign the window to the pager control with the [**PGM\_SETCHILD**](pgm-setchild.md) message.</span></span> <span data-ttu-id="47204-122">Tenga en cuenta que este mensaje no cambia realmente la ventana primaria de la ventana contenida; simplemente asigna la ventana contenida.</span><span class="sxs-lookup"><span data-stu-id="47204-122">Be aware that this message does not actually change the parent window of the contained window; it simply assigns the contained window.</span></span> <span data-ttu-id="47204-123">Si la ventana contenida es uno de los controles comunes, debe tener el estilo [**CCS \_ NORESIZE**](common-control-styles.md) para evitar que el control intente cambiar su tamaño al tamaño del control de paginación.</span><span class="sxs-lookup"><span data-stu-id="47204-123">If the contained window is one of the common controls, it must have the [**CCS\_NORESIZE**](common-control-styles.md) style to prevent the control from attempting to resize itself to the pager control's size.</span></span>

### <a name="process-pager-control-notifications"></a><span data-ttu-id="47204-124">Procesar notificaciones del control de buscapersonas</span><span class="sxs-lookup"><span data-stu-id="47204-124">Process Pager Control Notifications</span></span>

<span data-ttu-id="47204-125">Como mínimo, es necesario procesar la notificación de [ \_ CALCSIZE de PGN](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="47204-125">At a minimum, it is necessary to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification.</span></span> <span data-ttu-id="47204-126">Si no procesa esta notificación y especifica un valor para el ancho o el alto, no se mostrarán las flechas de desplazamiento en el control de paginación.</span><span class="sxs-lookup"><span data-stu-id="47204-126">If you do not process this notification and enter a value for the width or height, the scroll arrows in the pager control will not be displayed.</span></span> <span data-ttu-id="47204-127">Esto se debe a que el control de paginación utiliza el ancho o el alto proporcionado en la notificación de CALCSIZE de PGN \_ para determinar el tamaño "ideal" de la ventana contenida.</span><span class="sxs-lookup"><span data-stu-id="47204-127">This is because the pager control uses the width or height supplied in the PGN\_CALCSIZE notification to determine the "ideal" size of the contained window.</span></span>

<span data-ttu-id="47204-128">En el ejemplo siguiente se muestra cómo procesar el caso de notificación [PGN \_ CALCSIZE](pgn-calcsize.md) .</span><span class="sxs-lookup"><span data-stu-id="47204-128">The following example demonstrates how to process the [PGN\_CALCSIZE](pgn-calcsize.md) notification case.</span></span> <span data-ttu-id="47204-129">En este ejemplo, la ventana contenida es un control de barra de herramientas que contiene un número desconocido de botones con un tamaño desconocido.</span><span class="sxs-lookup"><span data-stu-id="47204-129">In this example, the contained window is a toolbar control that contains an unknown number of buttons at an unknown size.</span></span> <span data-ttu-id="47204-130">En el ejemplo se muestra cómo usar el mensaje [**TB \_ GETMAXSIZE**](tb-getmaxsize.md) para determinar el tamaño de todos los elementos de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="47204-130">The example shows how to use the [**TB\_GETMAXSIZE**](tb-getmaxsize.md) message to determine the size of all of the items in the toolbar.</span></span> <span data-ttu-id="47204-131">A continuación, el ejemplo coloca el ancho de todos los elementos en el miembro **iWidth** de la estructura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) que se pasa a la notificación.</span><span class="sxs-lookup"><span data-stu-id="47204-131">The example then places the width of all of the items into the **iWidth** member of the [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that is passed to the notification.</span></span>


```C++
case PGN_SCROLL:{

    LPNMPGSCROLL pScroll = (LPNMPGSCROLL)lParam;
 
    switch(pScroll->iDir){
     
        case PGF_SCROLLLEFT:
        case PGF_SCROLLRIGHT:
        case PGF_SCROLLUP:
        case PGF_SCROLLDOWN:
     
            pScroll->iScroll = 20;
        
            break;
        }
    }
  
return 0;
```



## <a name="related-topics"></a><span data-ttu-id="47204-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47204-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47204-133">Usar controles de buscapersonas</span><span class="sxs-lookup"><span data-stu-id="47204-133">Using Pager Controls</span></span>](using-pager-controls.md)
</dt> <dt>

<span data-ttu-id="47204-134">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="47204-134">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 