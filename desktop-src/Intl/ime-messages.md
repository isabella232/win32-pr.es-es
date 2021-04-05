---
description: El sistema operativo envía mensajes de la ventana del IME al procedimiento de ventana de una aplicación cuando se producen determinados eventos que afectan a las ventanas del IME.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: Mensajes IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f30baa01081e0aca1423f3384926938e6fdc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082192"
---
# <a name="ime-messages"></a><span data-ttu-id="7094d-103">Mensajes IME</span><span class="sxs-lookup"><span data-stu-id="7094d-103">IME Messages</span></span>

<span data-ttu-id="7094d-104">El sistema operativo envía mensajes de la ventana del IME al procedimiento de ventana de una aplicación cuando se producen determinados eventos que afectan a las ventanas del IME.</span><span class="sxs-lookup"><span data-stu-id="7094d-104">The operating system sends IME window messages to the window procedure of an application when certain events occur that affect the IME windows.</span></span> <span data-ttu-id="7094d-105">Por ejemplo, el sistema operativo envía el mensaje de la aplicación del [**\_ \_ IME de WM**](wm-ime-setcontext.md) a la aplicación cuando se activa una ventana.</span><span class="sxs-lookup"><span data-stu-id="7094d-105">For example, the operating system sends the [**WM\_IME\_SETCONTEXT**](wm-ime-setcontext.md) message to the application when a window is activated.</span></span> <span data-ttu-id="7094d-106">Las aplicaciones que no reconocen IME pasan estos mensajes a la función [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , que los envía a la ventana IME predeterminada correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7094d-106">IME-unaware applications pass these messages to the [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function, which sends them to the corresponding default IME window.</span></span> <span data-ttu-id="7094d-107">Las aplicaciones que tienen en cuenta el IME procesan estos mensajes o los reenvían a sus propias ventanas de IME.</span><span class="sxs-lookup"><span data-stu-id="7094d-107">IME-aware applications either process these messages or forward them to their own IME windows.</span></span>

<span data-ttu-id="7094d-108">La aplicación puede dirigir una ventana del IME para llevar a cabo un comando, por ejemplo, cambiar la posición de una ventana de composición mediante el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) .</span><span class="sxs-lookup"><span data-stu-id="7094d-108">Your application can direct an IME window to carry out a command, for example, change the position of a composition window, by using the [**WM\_IME\_CONTROL**](wm-ime-control.md) message.</span></span> <span data-ttu-id="7094d-109">El IME notifica a la aplicación los cambios en la cadena de composición mediante el mensaje de [**\_ \_ composición del IME de WM**](wm-ime-composition.md) y los cambios generales en el estado de las ventanas del IME mediante el envío del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7094d-109">The IME notifies the application about changes to the composition string by using the [**WM\_IME\_COMPOSITION**](wm-ime-composition.md) message, and about general changes to the status of the IME windows by sending the [**WM\_IME\_NOTIFY**](wm-ime-notify.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7094d-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7094d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7094d-111">Acerca del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="7094d-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
