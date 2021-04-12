---
title: Cómo crear un control de dirección IP
description: En este tema se muestra cómo crear una instancia de un control de dirección IP.
ms.assetid: E4DBECA6-B3F2-405F-8D95-32FA2334114D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8427a5695c0b9c79c19d328f4abc2ab0ffb2e5a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149738"
---
# <a name="how-to-create-an-ip-address-control"></a><span data-ttu-id="2e022-103">Cómo crear un control de dirección IP</span><span class="sxs-lookup"><span data-stu-id="2e022-103">How to Create an IP Address Control</span></span>

<span data-ttu-id="2e022-104">En este tema se muestra cómo crear una instancia de un control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="2e022-104">This topic demonstrates how to create an instance of an IP address control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2e022-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="2e022-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2e022-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="2e022-106">Technologies</span></span>

-   [<span data-ttu-id="2e022-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="2e022-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2e022-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2e022-108">Prerequisites</span></span>

-   <span data-ttu-id="2e022-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="2e022-109">C/C++</span></span>
-   <span data-ttu-id="2e022-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="2e022-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2e022-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="2e022-111">Instructions</span></span>


<span data-ttu-id="2e022-112">Antes de crear un control de dirección IP, cargue el archivo DLL de controles comunes llamando a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span><span class="sxs-lookup"><span data-stu-id="2e022-112">Before creating an IP address control, load the common controls DLL by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="2e022-113">A continuación, use la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de dirección IP de instancia.</span><span class="sxs-lookup"><span data-stu-id="2e022-113">Then use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an instance IP address control.</span></span> <span data-ttu-id="2e022-114">El nombre de clase del control es [**WC \_ IPAddress**](common-control-window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="2e022-114">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md).</span></span> <span data-ttu-id="2e022-115">Use el [**estilo \_ secundario WS**](/windows/desktop/winmsg/window-styles) , ya que no hay ninguna constante de estilo específica asociada con el control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="2e022-115">Use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style, because there is no specific style constant associated with the IP address control.</span></span>

<span data-ttu-id="2e022-116">En el siguiente ejemplo de código de C++, la función definida por la aplicación llama primero a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) y establece el miembro **dwICC** de la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) en [**\_ \_ las clases de Internet de ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), que especifica la clase de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="2e022-116">In the following C++ code example, the application-defined function first calls [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) and sets the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure to [**ICC\_INTERNET\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), which specifies the IP address class.</span></span> <span data-ttu-id="2e022-117">A continuación, llama a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear una instancia del control de dirección IP.</span><span class="sxs-lookup"><span data-stu-id="2e022-117">It then calls [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to create an instance of the IP address control.</span></span>


```C++
// CreateIPAdressFld - creates a IPAddress control.
// Returns the handle to the new control
// TO DO:  calling procedure needs to check whether the handle is NULL, in case 
// of an error in creation.
// int xcoord, ycoord the coordinates of location of the control in the parent window
// HINST hInst is the global handle to the application instance.
// HWND  hWndParent is the handle to the control's parent window. 
//
//
HWND CreateIPAddressFld (HWND hwndParent, int xcoord, int ycoord) 
{     
     
    INITCOMMONCONTROLSEX icex;
    
    // Ensure that the common control DLL is loaded. 
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC  = ICC_INTERNET_CLASSES ;
    InitCommonControlsEx(&icex); 
    
    // Create the IPAddress control.        
    HWND hWndIPAddressFld = CreateWindow(WC_IPADDRESS, 
                                L"", 
                                WS_CHILD | WS_OVERLAPPED | WS_VISIBLE, 
                                xcoord, 
                                ycoord,
                                150, 
                                20,  
                                hwndParent, 
                                NULL, 
                                hInst, 
                                NULL); 
                                
    return (hWndIPAddressFld);
}
```



## <a name="related-topics"></a><span data-ttu-id="2e022-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e022-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e022-119">Referencia de control de dirección IP</span><span class="sxs-lookup"><span data-stu-id="2e022-119">IP Address Control Reference</span></span>](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[<span data-ttu-id="2e022-120">Acerca de los controles de dirección IP</span><span class="sxs-lookup"><span data-stu-id="2e022-120">About IP Address Controls</span></span>](ip-address-controls.md)
</dt> <dt>

[<span data-ttu-id="2e022-121">Usar controles de direcciones IP</span><span class="sxs-lookup"><span data-stu-id="2e022-121">Using IP Address Controls</span></span>](using-ip-address-controls.md)
</dt> </dl>

 

 