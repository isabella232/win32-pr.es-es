---
title: Cómo recuperar y establecer una tecla de acceso rápido
description: En este tema se muestra cómo recuperar o establecer la combinación de teclas de un control de tecla de acceso rápido.
ms.assetid: F3643196-F847-4EE4-97ED-75AF52D4FF8D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d453433917c211bc787f70a5d9344f1a477858e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105656443"
---
# <a name="how-to-retrieve-and-set-a-hot-key"></a><span data-ttu-id="ea37c-103">Cómo recuperar y establecer una tecla de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="ea37c-103">How to Retrieve and Set a Hot Key</span></span>

<span data-ttu-id="ea37c-104">En este tema se muestra cómo recuperar o establecer la combinación de teclas de un control de tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="ea37c-104">This topic demonstrates how to retrieve or set the key combination for a hot key control.</span></span> <span data-ttu-id="ea37c-105">El mensaje [**HKM \_ SETHOTKEY**](hkm-sethotkey.md) permite a una aplicación establecer la combinación de teclas de acceso rápido para un control de tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="ea37c-105">The [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message allows an application to set the hot key combination for a hot key control.</span></span> <span data-ttu-id="ea37c-106">Las aplicaciones usan el mensaje [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) para recuperar el código de tecla virtual y los marcadores modificadores de la tecla de acceso rápido que el usuario elige.</span><span class="sxs-lookup"><span data-stu-id="ea37c-106">Applications use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier flags of the hot key that is chosen by the user.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ea37c-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="ea37c-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ea37c-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="ea37c-108">Technologies</span></span>

-   [<span data-ttu-id="ea37c-109">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="ea37c-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="ea37c-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea37c-110">Prerequisites</span></span>

-   <span data-ttu-id="ea37c-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="ea37c-111">C/C++</span></span>
-   <span data-ttu-id="ea37c-112">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="ea37c-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="ea37c-113">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ea37c-113">Instructions</span></span>


<span data-ttu-id="ea37c-114">Use el mensaje [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) para recuperar el código de tecla virtual y las teclas modificadoras que describen una tecla de acceso rápido elegida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ea37c-114">Use the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve the virtual key code and modifier keys that describe a hot key chosen by the user.</span></span> <span data-ttu-id="ea37c-115">Use el [**mensaje \_ SETHOTKEY de HKM**](hkm-sethotkey.md) para establecer los valores de una tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="ea37c-115">Use the [**HKM\_SETHOTKEY**](hkm-sethotkey.md) message to set those values for a hot key.</span></span>

<span data-ttu-id="ea37c-116">En el siguiente ejemplo de código de C++, la función definida por la aplicación utiliza el mensaje [**\_ GETHOTKEY de HKM**](hkm-gethotkey.md) para recuperar una combinación de teclas de un control de tecla de acceso rápido y, a continuación, usa el mensaje de [**\_ SETHOTKEY de WM**](/windows/desktop/inputdev/wm-sethotkey) para establecer una tecla de acceso rápido global.</span><span class="sxs-lookup"><span data-stu-id="ea37c-116">In the following C++ code example, the application-defined function uses the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message to retrieve a key combination from a hot key control and then uses the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message to set a global hot key.</span></span> <span data-ttu-id="ea37c-117">Tenga en cuenta que no puede establecer una tecla de acceso rápido global para una ventana que tenga el estilo de ventana [**\_ secundaria de WS**](/windows/desktop/winmsg/window-styles) .</span><span class="sxs-lookup"><span data-stu-id="ea37c-117">Note that you cannot set a global hot key for a window that has the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) window style.</span></span>



```C++
// Retrieves the hot key from the hot key control and sets it as
// the hot key for the application's main window. 
//
// Parameters 
//     hwndHot  - Handle of the hot key control. 
//     hwndMain - Handle of the main window. 

BOOL WINAPI ProcessHotkey(HWND hwndHot, HWND hwndMain) 
{ 
    WORD wHotkey;  

    // Retrieve the hot key (virtual key code and modifiers). 
    wHotkey = (WORD) SendMessage(hwndHot, HKM_GETHOTKEY, 0, 0); 
    
    // Use the result as wParam for WM_SETHOTKEY. 
    SendMessage(hwndMain, WM_SETHOTKEY, wHotkey, 0); 
    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="ea37c-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea37c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea37c-119">Referencia de control de teclas de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="ea37c-119">Hot Key Control Reference</span></span>](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ea37c-120">Acerca de los controles de tecla de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="ea37c-120">About Hot Key Controls</span></span>](hot-key-controls.md)
</dt> <dt>

[<span data-ttu-id="ea37c-121">Usar controles de tecla de acceso rápido</span><span class="sxs-lookup"><span data-stu-id="ea37c-121">Using Hot Key Controls</span></span>](using-hot-key-controls.md)
</dt> </dl>

 

 