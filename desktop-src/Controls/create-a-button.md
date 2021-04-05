---
title: Cómo crear un botón
description: Para crear botones dinámicamente, se usa la función CreateWindow o CreateWindowEx. En este tema se muestra cómo usar la función CreateWindow para crear un botón de método de envío predeterminado.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078632"
---
# <a name="how-to-create-a-button"></a><span data-ttu-id="7f2f0-104">Cómo crear un botón</span><span class="sxs-lookup"><span data-stu-id="7f2f0-104">How to Create a Button</span></span>

<span data-ttu-id="7f2f0-105">Para crear botones dinámicamente, se usa la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="7f2f0-105">To create buttons dynamically, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="7f2f0-106">En este tema se muestra cómo usar la función **CreateWindow** para crear un botón de método de envío predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7f2f0-106">This topic demonstrates how to use the **CreateWindow** function to create a default push button.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7f2f0-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="7f2f0-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7f2f0-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="7f2f0-108">Technologies</span></span>

-   [<span data-ttu-id="7f2f0-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="7f2f0-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7f2f0-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7f2f0-110">Prerequisites</span></span>

-   <span data-ttu-id="7f2f0-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="7f2f0-111">C/C++</span></span>
-   <span data-ttu-id="7f2f0-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="7f2f0-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7f2f0-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="7f2f0-113">Instructions</span></span>


<span data-ttu-id="7f2f0-114">Utilice la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) para crear un control de botón.</span><span class="sxs-lookup"><span data-stu-id="7f2f0-114">Use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function to create a button control.</span></span>

<span data-ttu-id="7f2f0-115">En el siguiente ejemplo de C++, el parámetro *\_ hWnd de m* es el identificador de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="7f2f0-115">In the following C++ example, the *m\_hwnd* parameter is the handle to the parent window.</span></span> <span data-ttu-id="7f2f0-116">El estilo [**BS \_ DEFPUSHBUTTON**](button-styles.md) especifica que se debe crear un botón de envío predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7f2f0-116">The [**BS\_DEFPUSHBUTTON**](button-styles.md) style specifies that a default push button should be created.</span></span> <span data-ttu-id="7f2f0-117">Tenga en cuenta que los valores de tamaño y posición deben especificarse porque el uso de **CW \_ USEDEFAULT** para un botón establece los valores en cero.</span><span class="sxs-lookup"><span data-stu-id="7f2f0-117">Note that the size and position values must be specified because using **CW\_USEDEFAULT** for a button sets the values to zero.</span></span>


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
```



## <a name="related-topics"></a><span data-ttu-id="7f2f0-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f2f0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f2f0-119">Acerca de los botones</span><span class="sxs-lookup"><span data-stu-id="7f2f0-119">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="7f2f0-120">Referencia de control de botón</span><span class="sxs-lookup"><span data-stu-id="7f2f0-120">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="7f2f0-121">Usar botones</span><span class="sxs-lookup"><span data-stu-id="7f2f0-121">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="7f2f0-122">Botón</span><span class="sxs-lookup"><span data-stu-id="7f2f0-122">Button</span></span>](buttons.md)
</dt> </dl>

 

 