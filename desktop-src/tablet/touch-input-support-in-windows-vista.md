---
description: A partir de Windows Vista, la tecnología de Tablet PC es compatible con la entrada táctil en Tablet PC con digitalizadores táctiles. Esta compatibilidad incluye una interfaz de usuario mejorada para ayudar a dirigir y a las ventanas de comandos cuando se usa un dedo para la entrada.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Compatibilidad con la entrada táctil en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b623630c93c33b846ab1bb491fc56fe46dfe825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706569"
---
# <a name="touch-input-support-in-windows-vista"></a><span data-ttu-id="e0ae9-104">Compatibilidad con la entrada táctil en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0ae9-104">Touch Input Support in Windows Vista</span></span>

<span data-ttu-id="e0ae9-105">A partir de Windows Vista, la tecnología de Tablet PC es compatible con la entrada táctil en Tablet PC con digitalizadores táctiles.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-105">Starting with Windows Vista, Tablet PC Technology has support for touch input on Tablet PC's with touch capable digitizers.</span></span> <span data-ttu-id="e0ae9-106">Esta compatibilidad incluye una interfaz de usuario mejorada para ayudar a dirigir y a las ventanas de comandos cuando se usa un dedo para la entrada.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-106">This support includes an enhanced user interface to aid in targeting and commanding Windows when using a finger for input.</span></span>

## <a name="touch-digitizer-support"></a><span data-ttu-id="e0ae9-107">Compatibilidad con el digitalizador táctil</span><span class="sxs-lookup"><span data-stu-id="e0ae9-107">Touch Digitizer Support</span></span>

### <a name="pen-and-touch-input-not-exclusive"></a><span data-ttu-id="e0ae9-108">Lápiz y entrada táctil no exclusiva</span><span class="sxs-lookup"><span data-stu-id="e0ae9-108">Pen and Touch Input Not Exclusive</span></span>

<span data-ttu-id="e0ae9-109">No asuma que el lápiz y la entrada táctil se excluyen mutuamente en las aplicaciones [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)y [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e0ae9-109">Do not assume pen and touch input are mutually exclusive in [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), and [**RealTimeStylus**](realtimestylus-class.md) applications.</span></span>

<span data-ttu-id="e0ae9-110">En Windows Vista, cuando el sistema reconoce un lápiz, omite la entrada táctil.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-110">In Windows Vista, when the system recognizes a pen it ignores touch input.</span></span> <span data-ttu-id="e0ae9-111">Es decir, el trazo táctil finaliza y comienza el trazo del lápiz.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-111">That is, the touch stroke ends and the pen stroke begins.</span></span> <span data-ttu-id="e0ae9-112">Como esto podría cambiar en el futuro, el código no debe asumir que el lápiz y la entrada táctil se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-112">Because this could possibly change in the future, your code should not assume pen and touch input are mutually exclusive.</span></span>

### <a name="other-mouse-message-sources"></a><span data-ttu-id="e0ae9-113">Otros orígenes de mensajes del mouse</span><span class="sxs-lookup"><span data-stu-id="e0ae9-113">Other Mouse Message Sources</span></span>

<span data-ttu-id="e0ae9-114">Hay otros orígenes de mensajes del mouse incluso cuando el usuario solo está interactuando con el dedo o el lápiz.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-114">There are other sources of mouse messages even when the user is only interacting using finger or pen.</span></span> <span data-ttu-id="e0ae9-115">Los orígenes incluyen touchpad, así como el movimiento diseñado para permitir que una aplicación detrás de una ventana superpuesta tenga en cuenta que el mouse se mueve sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-115">Sources include touchpads, as well as movement intended to let an application behind a layered window be aware that the mouse is moving above the application.</span></span>

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a><span data-ttu-id="e0ae9-116">Habilitación y deshabilitación de la interfaz de usuario de entrada táctil</span><span class="sxs-lookup"><span data-stu-id="e0ae9-116">Enabling and Disabling the Touch Input User Interface</span></span>

<span data-ttu-id="e0ae9-117">Puede habilitar o deshabilitar la interfaz de usuario de entrada táctil en función de los requisitos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-117">You may wish to enable or disable the touch input user interface depending on the requirements of your application.</span></span> <span data-ttu-id="e0ae9-118">Para ello, intercepte los mensajes de ventana del sistema operativo en un procedimiento de ventana y modifique el mensaje de Windows.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-118">To accomplish this, intercept operating system window messages in a window procedure and modify the Windows message.</span></span> <span data-ttu-id="e0ae9-119">Invalide [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) en la aplicación para interceptar estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-119">Override [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) in your application to intercept these messages.</span></span> <span data-ttu-id="e0ae9-120">En el siguiente \# pseudocódigo de C se muestra cómo habilitar y deshabilitar la interfaz de usuario de entrada táctil.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-120">The following C\# pseudo-code shows how to enable and disable the touch input user interface.</span></span> <span data-ttu-id="e0ae9-121">El código también muestra cómo usar la misma técnica para deshabilitar el gesto de mantener presionado.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-121">The code also shows using the same technique to disable the press-and-hold gesture.</span></span> <span data-ttu-id="e0ae9-122">Este método también sirve para deshabilitar el lápiz.</span><span class="sxs-lookup"><span data-stu-id="e0ae9-122">This method also works for disabling the stylus.</span></span>


```C++
const int WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS = 716;

const uint SYSTEM_GESTURE_STATUS_NOHOLD           = 0x00000001;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON  = 0x00000100;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF = 0x00000200;

protected override void WndProc(ref Message msg)
{
    switch (msg.Msg)
    {
        case WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS:
        {
            uint result = 0;
            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_NOHOLD;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF;
            }

            msg.Result = (IntPtr)result;
        }
        break;

        default:
            base.WndProc(ref msg);
            break;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="e0ae9-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0ae9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0ae9-124">Windows Touch</span><span class="sxs-lookup"><span data-stu-id="e0ae9-124">Windows Touch</span></span>](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
