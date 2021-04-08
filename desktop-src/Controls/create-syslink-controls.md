---
title: Cómo crear controles SysLink
description: Los hipervínculos del control SysLink se implementan mediante el marcado de la cadena de inicialización del control o mediante el envío de un \_ mensaje SETITEM de LM.
ms.assetid: CEE02A87-D85A-4F4D-931D-2B1371320814
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa5c5ff3348f35f9c67cb34bea0cc495d403ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794140"
---
# <a name="how-to-create-syslink-controls"></a><span data-ttu-id="8bf48-103">Cómo crear controles SysLink</span><span class="sxs-lookup"><span data-stu-id="8bf48-103">How to Create SysLink Controls</span></span>

<span data-ttu-id="8bf48-104">Los hipervínculos del control SysLink se implementan mediante el marcado de la cadena de inicialización del control o mediante el envío de un mensaje [**\_ SETITEM de LM**](lm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="8bf48-104">You implement the SysLink control's hyperlinks through markup in the control's initialization string, or by sending it a [**LM\_SETITEM**](lm-setitem.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="8bf48-105">Antes de crear los controles SysLink, debe llamar a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) , especificando la \_ clase de vínculo ICC \_ .</span><span class="sxs-lookup"><span data-stu-id="8bf48-105">Before creating SysLink controls, you must call the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function, specifying the ICC\_LINK\_CLASS.</span></span>

 

<span data-ttu-id="8bf48-106">Para crear un SysLink, llame a la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando la clase de ventana de [**\_ vínculo de CT**](common-control-window-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="8bf48-106">To create a SysLink, call the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_LINK**](common-control-window-classes.md) window class.</span></span> <span data-ttu-id="8bf48-107">El parámetro *lpWindowName* que es común a estas funciones especifica un puntero a una cadena terminada en cero que contiene el texto marcado que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="8bf48-107">The *lpWindowName* parameter that is common to these functions specifies a pointer to a zero-terminated string that contains the marked-up text to display.</span></span> <span data-ttu-id="8bf48-108">Para los estilos de ventana concretos de los controles SysLink, consulte [estilos de control syslink](syslink-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="8bf48-108">For window styles particular to SysLink controls, see [SysLink Control Styles](syslink-control-styles.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8bf48-109">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="8bf48-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8bf48-110">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="8bf48-110">Technologies</span></span>

-   [<span data-ttu-id="8bf48-111">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="8bf48-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8bf48-112">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8bf48-112">Prerequisites</span></span>

-   <span data-ttu-id="8bf48-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="8bf48-113">C/C++</span></span>
-   <span data-ttu-id="8bf48-114">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="8bf48-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8bf48-115">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="8bf48-115">Instructions</span></span>

### <a name="create-a-syslink-control"></a><span data-ttu-id="8bf48-116">Crear un control SysLink</span><span class="sxs-lookup"><span data-stu-id="8bf48-116">Create a SysLink Control</span></span>

<span data-ttu-id="8bf48-117">En el código de ejemplo siguiente se crea un control SysLink que muestra dos hipervínculos.</span><span class="sxs-lookup"><span data-stu-id="8bf48-117">The following example code creates a SysLink control that displays two hyperlinks.</span></span> <span data-ttu-id="8bf48-118">El primer hipervínculo es una dirección URL de Internet y el segundo es definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8bf48-118">The first hyperlink is an Internet URL, and the second is application-defined.</span></span>


```C++
HWND CreateSysLink(HWND hDlg, HINSTANCE hInst, RECT rect)
{
    return CreateWindowEx(0, WC_LINK, 
        L"For more information, <A HREF=\"https://www.microsoft.com\">click here</A> " \
        L"or <A ID=\"idInfo\">here</A>.", 
        WS_VISIBLE | WS_CHILD | WS_TABSTOP, 
        rect.left, rect.top, rect.right, rect.bottom, 
        hDlg, NULL, hInst, NULL);
}
```



## <a name="remarks"></a><span data-ttu-id="8bf48-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bf48-119">Remarks</span></span>

<span data-ttu-id="8bf48-120">Se supone que ya se ha llamado a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="8bf48-120">It is assumed that [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) has already been called.</span></span>

<span data-ttu-id="8bf48-121">Al especificar el estilo de [**WS \_ TABSTOP**](/windows/desktop/winmsg/window-styles) , se asegura de que el usuario podrá seleccionar un vínculo con el tabulador y presionar la tecla entrar.</span><span class="sxs-lookup"><span data-stu-id="8bf48-121">Specifying the [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) style ensures that the user will be able to select a link by tabbing to it and pressing the Enter key.</span></span>

<span data-ttu-id="8bf48-122">La versión 6 de ComCtl32.dll solo es compatible con Unicode.</span><span class="sxs-lookup"><span data-stu-id="8bf48-122">Version 6 of ComCtl32.dll supports Unicode only.</span></span> <span data-ttu-id="8bf48-123">Por lo tanto, no se pueden crear versiones ANSI de controles SysLink, solo Unicode.</span><span class="sxs-lookup"><span data-stu-id="8bf48-123">Therefore, you cannot create ANSI versions of SysLink controls—only Unicode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bf48-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8bf48-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bf48-125">Usar controles SysLink</span><span class="sxs-lookup"><span data-stu-id="8bf48-125">Using SysLink Controls</span></span>](/windows/desktop/Controls/using-syslink-controls)
</dt> <dt>

<span data-ttu-id="8bf48-126">[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="8bf48-126">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 