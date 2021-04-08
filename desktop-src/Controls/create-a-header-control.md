---
title: Cómo crear un control de encabezado
description: En este tema se muestra cómo crear un control de encabezado y colocarlo en el área de cliente de la ventana primaria.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9bf9d7b117f5f61766ca326b91b0d19a2c903
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078631"
---
# <a name="how-to-create-a-header-control"></a><span data-ttu-id="3fbdb-103">Cómo crear un control de encabezado</span><span class="sxs-lookup"><span data-stu-id="3fbdb-103">How to Create a Header Control</span></span>

<span data-ttu-id="3fbdb-104">En este tema se muestra cómo crear un control de encabezado y colocarlo en el área de cliente de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="3fbdb-104">This topic demonstrates how to create a header control and position it within the parent window's client area.</span></span> <span data-ttu-id="3fbdb-105">Puede crear un control de encabezado mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especificando la clase de ventana de [**\_ encabezado WC**](common-control-window-classes.md) y los [estilos de control de encabezado](header-control-styles.md)adecuados.</span><span class="sxs-lookup"><span data-stu-id="3fbdb-105">You can create a header control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying the [**WC\_HEADER**](common-control-window-classes.md) window class and the appropriate [header control styles](header-control-styles.md).</span></span> <span data-ttu-id="3fbdb-106">Esta clase de ventana se registra cuando se carga el archivo DLL de control común.</span><span class="sxs-lookup"><span data-stu-id="3fbdb-106">This window class is registered when the common control DLL is loaded.</span></span> <span data-ttu-id="3fbdb-107">Para asegurarse de que se carga este archivo DLL, utilice la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="3fbdb-107">To ensure that this DLL is loaded, use the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="3fbdb-108">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="3fbdb-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="3fbdb-109">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="3fbdb-109">Technologies</span></span>

-   [<span data-ttu-id="3fbdb-110">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="3fbdb-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="3fbdb-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3fbdb-111">Prerequisites</span></span>

-   <span data-ttu-id="3fbdb-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="3fbdb-112">C/C++</span></span>
-   <span data-ttu-id="3fbdb-113">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="3fbdb-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="3fbdb-114">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="3fbdb-114">Instructions</span></span>


<span data-ttu-id="3fbdb-115">En el siguiente ejemplo de código de C++ se llama primero a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para cargar el archivo dll de control común.</span><span class="sxs-lookup"><span data-stu-id="3fbdb-115">The following C++ code example first calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="3fbdb-116">A continuación, llama a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de encabezado.</span><span class="sxs-lookup"><span data-stu-id="3fbdb-116">It then calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a header control.</span></span> <span data-ttu-id="3fbdb-117">El control está oculto inicialmente.</span><span class="sxs-lookup"><span data-stu-id="3fbdb-117">The control is initially hidden.</span></span> <span data-ttu-id="3fbdb-118">El mensaje de [**\_ diseño HDM**](hdm-layout.md) se usa para calcular el tamaño y la posición del control dentro de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="3fbdb-118">The [**HDM\_LAYOUT**](hdm-layout.md) message is used to calculate the size and position of the control within the parent window.</span></span> <span data-ttu-id="3fbdb-119">Después, el control cambia de posición y se hace visible.</span><span class="sxs-lookup"><span data-stu-id="3fbdb-119">The control is then repositioned and made visible.</span></span>



```C++
// DoCreateHeader - creates a header control that is positioned along 
//     the top of the parent window's client area. 
// Returns the handle to the header control. 
// hwndParent - handle to the parent window. 
// 
// Global variable 
//    g_hinst - handle to the application instance 
extern HINSTANCE g_hinst; 
//
// child-window identifier
int ID_HEADER;
//
HWND DoCreateHeader(HWND hwndParent) 
{ 
        HWND hwndHeader; 
        RECT rcParent; 
        HDLAYOUT hdl; 
        WINDOWPOS wp; 
 
        // Ensure that the common control DLL is loaded, and then create 
        // the header control. 
        INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
        icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
        icex.dwICC = ICC_LISTVIEW_CLASSES;   //set dwICC member to ICC_LISTVIEW_CLASSES    
                                             // this loads list-view and header control classes.
    InitCommonControlsEx(&icex); 
 
        if ((hwndHeader = CreateWindowEx(0, WC_HEADER, (LPCTSTR) NULL, 
                WS_CHILD | WS_BORDER | HDS_BUTTONS | HDS_HORZ, 
                0, 0, 0, 0, hwndParent, (HMENU) ID_HEADER, g_hinst, 
                (LPVOID) NULL)) == NULL) 
            return (HWND) NULL; 
 
        // Retrieve the bounding rectangle of the parent window's 
        // client area, and then request size and position values 
        // from the header control. 
        GetClientRect(hwndParent, &rcParent); 
 
        hdl.prc = &rcParent; 
        hdl.pwpos = &wp; 
        if (!SendMessage(hwndHeader, HDM_LAYOUT, 0, (LPARAM) &hdl)) 
            return (HWND) NULL; 
 
        // Set the size, position, and visibility of the header control. 
        SetWindowPos(hwndHeader, wp.hwndInsertAfter, wp.x, wp.y, 
            wp.cx, wp.cy, wp.flags | SWP_SHOWWINDOW); 
 
        return hwndHeader; 
}
```



## <a name="related-topics"></a><span data-ttu-id="3fbdb-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3fbdb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fbdb-121">Acerca de los controles de encabezado</span><span class="sxs-lookup"><span data-stu-id="3fbdb-121">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="3fbdb-122">Referencia de control de encabezado</span><span class="sxs-lookup"><span data-stu-id="3fbdb-122">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="3fbdb-123">Usar controles de encabezado</span><span class="sxs-lookup"><span data-stu-id="3fbdb-123">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 