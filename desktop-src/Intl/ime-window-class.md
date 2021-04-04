---
description: La clase de ventana IME es una clase global del sistema predefinida que define la apariencia y el comportamiento de las ventanas del IME estándar.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: Clase de ventana IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faae7fd0135ec894186b4e10df9bc02da66bb933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910118"
---
# <a name="ime-window-class"></a><span data-ttu-id="46970-103">Clase de ventana IME</span><span class="sxs-lookup"><span data-stu-id="46970-103">IME Window Class</span></span>

<span data-ttu-id="46970-104">La clase de ventana IME es una clase global del sistema predefinida que define la apariencia y el comportamiento de las ventanas del IME estándar.</span><span class="sxs-lookup"><span data-stu-id="46970-104">The IME window class is a predefined system global class that defines the appearance and behavior of the standard IME windows.</span></span> <span data-ttu-id="46970-105">La clase es similar a las clases de controles comunes en que la aplicación crea una ventana de esta clase mediante la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="46970-105">The class is similar to common control classes in that the application creates a window of this class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="46970-106">Al igual que los controles estáticos, una ventana del IME no responde a la entrada del usuario por sí sola.</span><span class="sxs-lookup"><span data-stu-id="46970-106">Like static controls, an IME window does not respond to user input by itself.</span></span> <span data-ttu-id="46970-107">En su lugar, notifica al IME las acciones de entrada del usuario y procesa los mensajes de control enviados por el IME o las aplicaciones para llevar a cabo una respuesta a la acción del usuario.</span><span class="sxs-lookup"><span data-stu-id="46970-107">Instead, it notifies the IME of user input actions and processes control messages sent to it by the IME or applications to carry out a response to the user action.</span></span>

<span data-ttu-id="46970-108">A veces, las aplicaciones que reconocen el IME crean ventanas de IME personalizadas mediante la clase de ventana de IME.</span><span class="sxs-lookup"><span data-stu-id="46970-108">IME-aware applications sometimes create customized IME windows using the IME window class.</span></span> <span data-ttu-id="46970-109">El uso de la personalización de ventanas permite a la aplicación aprovechar el procesamiento predeterminado de la ventana del IME mientras controla la posición de la ventana.</span><span class="sxs-lookup"><span data-stu-id="46970-109">Use of window customization allows the application to take advantage of the default processing of the IME window while having control of window positioning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46970-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="46970-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46970-111">Acerca del administrador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="46970-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
