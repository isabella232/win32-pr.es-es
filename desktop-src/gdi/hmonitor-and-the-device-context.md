---
description: Cada pantalla física se representa mediante un identificador de monitor de tipo HMONITOR.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR y el contexto del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da397af45b906a626f79f7b934b78aaad481f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997357"
---
# <a name="hmonitor-and-the-device-context"></a><span data-ttu-id="06e78-103">HMONITOR y el contexto del dispositivo</span><span class="sxs-lookup"><span data-stu-id="06e78-103">HMONITOR and the Device Context</span></span>

<span data-ttu-id="06e78-104">Cada pantalla física se representa mediante un identificador de monitor de tipo **HMONITOR**.</span><span class="sxs-lookup"><span data-stu-id="06e78-104">Each physical display is represented by a monitor handle of type **HMONITOR**.</span></span> <span data-ttu-id="06e78-105">Se garantiza que un **HMONITOR** válido no es NULL.</span><span class="sxs-lookup"><span data-stu-id="06e78-105">A valid **HMONITOR** is guaranteed to be non-NULL.</span></span> <span data-ttu-id="06e78-106">Una pantalla física tiene el mismo **HMONITOR** siempre que forme parte del escritorio.</span><span class="sxs-lookup"><span data-stu-id="06e78-106">A physical display has the same **HMONITOR** as long as it is part of the desktop.</span></span> <span data-ttu-id="06e78-107">Cuando se envía un mensaje de **\_ DISPLAYCHANGE de WM** , es posible que se quite cualquier monitor del escritorio y, por tanto, su **HMONITOR** deje de ser válido o se cambiara su configuración.</span><span class="sxs-lookup"><span data-stu-id="06e78-107">When a **WM\_DISPLAYCHANGE** message is sent, any monitor may be removed from the desktop and thus its **HMONITOR** becomes invalid or has its settings changed.</span></span> <span data-ttu-id="06e78-108">Por lo tanto, una aplicación debe comprobar si todos los **HMONITORS** son válidos cuando se envía este mensaje.</span><span class="sxs-lookup"><span data-stu-id="06e78-108">Therefore, an application should check whether all **HMONITORS** are valid when this message is sent.</span></span>

<span data-ttu-id="06e78-109">Cualquier función que devuelva un contexto de dispositivo de pantalla (DC) suele devolver un controlador de dominio para el monitor principal.</span><span class="sxs-lookup"><span data-stu-id="06e78-109">Any function that returns a display device context (DC) normally returns a DC for the primary monitor.</span></span> <span data-ttu-id="06e78-110">Para obtener el controlador de dominio para otro monitor, utilice la función [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .</span><span class="sxs-lookup"><span data-stu-id="06e78-110">To obtain the DC for another monitor, use the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span> <span data-ttu-id="06e78-111">O bien, puede usar el nombre del dispositivo de la función [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) para crear un controlador de dominio con [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca).</span><span class="sxs-lookup"><span data-stu-id="06e78-111">Or, you can use the device name from the [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) function to create a DC with [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="06e78-112">Sin embargo, si la función, como [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) o [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), obtiene un controlador de dominio para una ventana que abarca más de una pantalla, el controlador de dominio también abarcará las dos pantallas.</span><span class="sxs-lookup"><span data-stu-id="06e78-112">However, if the function, such as [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), gets a DC for a window that spans more than one display, the DC will also span the two displays.</span></span>

 

 



