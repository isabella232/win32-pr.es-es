---
title: Cómo crear un vínculo de comando
description: En este tema se describe una manera de crear un vínculo de comando.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8024a7f060a7bae3779b9ec9ebec40bd81c74bb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488394"
---
# <a name="how-to-create-a-command-link"></a><span data-ttu-id="a36dd-103">Cómo crear un vínculo de comando</span><span class="sxs-lookup"><span data-stu-id="a36dd-103">How to Create a Command Link</span></span>

<span data-ttu-id="a36dd-104">En este tema se describe una manera de crear un vínculo de comando.</span><span class="sxs-lookup"><span data-stu-id="a36dd-104">This topic describes one way to create a command link.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a36dd-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="a36dd-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a36dd-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="a36dd-106">Technologies</span></span>

-   [<span data-ttu-id="a36dd-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="a36dd-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a36dd-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a36dd-108">Prerequisites</span></span>

-   <span data-ttu-id="a36dd-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="a36dd-109">C/C++</span></span>
-   <span data-ttu-id="a36dd-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="a36dd-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a36dd-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="a36dd-111">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-command-link-button"></a><span data-ttu-id="a36dd-112">Paso 1: crear una instancia del botón de vínculo de comando.</span><span class="sxs-lookup"><span data-stu-id="a36dd-112">Step 1: Create an instance of the command link button.</span></span>

<span data-ttu-id="a36dd-113">En el siguiente ejemplo de código de C++, la constante de estilo [**BS \_ COMMANDLINK**](button-styles.md) especifica el botón como un botón de vínculo de comando.</span><span class="sxs-lookup"><span data-stu-id="a36dd-113">In the following C++ code example, the style constant [**BS\_COMMANDLINK**](button-styles.md) specifies the button as a command link button.</span></span>


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a><span data-ttu-id="a36dd-114">Paso 2: establecer la etiqueta del vínculo de comando y el texto de explicación</span><span class="sxs-lookup"><span data-stu-id="a36dd-114">Step 2: Set the command link label and explanation text</span></span>

<span data-ttu-id="a36dd-115">Utilice la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para establecer la etiqueta del vínculo de comando y el texto complementario mediante el mensaje de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) y el mensaje [**\_ SETNOTE de BCM**](bcm-setnote.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a36dd-115">Use the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function to set the command link label and supplementary text via the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message and the [**BCM\_SETNOTE**](bcm-setnote.md) message, respectively.</span></span>


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
```



## <a name="related-topics"></a><span data-ttu-id="a36dd-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a36dd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a36dd-117">Acerca de los botones</span><span class="sxs-lookup"><span data-stu-id="a36dd-117">About Buttons</span></span>](about-buttons.md)
</dt> <dt>

[<span data-ttu-id="a36dd-118">Referencia de control de botón</span><span class="sxs-lookup"><span data-stu-id="a36dd-118">Button Control Reference</span></span>](bumper-button-button-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a36dd-119">Usar botones</span><span class="sxs-lookup"><span data-stu-id="a36dd-119">Using Buttons</span></span>](using-buttons.md)
</dt> <dt>

[<span data-ttu-id="a36dd-120">Botón</span><span class="sxs-lookup"><span data-stu-id="a36dd-120">Button</span></span>](buttons.md)
</dt> </dl>

 

 