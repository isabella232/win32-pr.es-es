---
title: Cómo procesar notificaciones de ComboBoxEx
description: En este tema se muestra cómo procesar mensajes de notificación ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995776"
---
# <a name="how-to-process-comboboxex-notifications"></a><span data-ttu-id="32934-103">Cómo procesar notificaciones de ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="32934-103">How to Process ComboBoxEx Notifications</span></span>

<span data-ttu-id="32934-104">En este tema se muestra cómo procesar mensajes de notificación ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="32934-104">This topic demonstrates how to process ComboBoxEx notification messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="32934-105">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="32934-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="32934-106">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="32934-106">Technologies</span></span>

-   [<span data-ttu-id="32934-107">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="32934-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="32934-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="32934-108">Prerequisites</span></span>

-   <span data-ttu-id="32934-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="32934-109">C/C++</span></span>
-   <span data-ttu-id="32934-110">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="32934-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="32934-111">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="32934-111">Instructions</span></span>


<span data-ttu-id="32934-112">Un control ComboBoxEx notifica a su ventana primaria de eventos mediante el envío de mensajes de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="32934-112">A ComboBoxEx control notifies its parent window of events by sending [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="32934-113">También pasa los mensajes de notificación de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) que recibe del cuadro combinado que contiene en la ventana primaria que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="32934-113">It also passes the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages that it receives from the combo box contained within it to the parent window to be processed.</span></span> <span data-ttu-id="32934-114">Por lo tanto, la aplicación debe estar preparada para procesar mensajes de **\_ notificación de WM** desde los mensajes de **\_ comando** ComboBoxEx y WM que se reenvían desde el control de cuadro combinado secundario ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="32934-114">Therefore, your application must be prepared to process **WM\_NOTIFY** messages from the ComboBoxEx and **WM\_COMMAND** messages that are forwarded from the ComboBoxEx child combo box control.</span></span>

<span data-ttu-id="32934-115">En el ejemplo de esta sección se tratan los mensajes [**de \_ comandos**](/windows/desktop/menurc/wm-command) de [**\_ Notify**](wm-notify.md) y WM de WM desde un control ComboBoxEx mediante una llamada a una función definida por la aplicación correspondiente para procesar estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="32934-115">The example in this section handles the [**WM\_NOTIFY**](wm-notify.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages from a ComboBoxEx control by calling a corresponding application-defined function to process these messages.</span></span>

## <a name="complete-example"></a><span data-ttu-id="32934-116">Ejemplo completo</span><span class="sxs-lookup"><span data-stu-id="32934-116">Complete example</span></span>


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="32934-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32934-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32934-118">Acerca de los controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="32934-118">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="32934-119">Referencia de control ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="32934-119">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="32934-120">Usar controles ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="32934-120">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="32934-121">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="32934-121">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 