---
description: Además de la región de actualización, cada ventana tiene un área visible que define la parte de la ventana visible para el usuario.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Regiones de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02555339412c604f79f69294febbab524fc92a70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083040"
---
# <a name="window-regions"></a><span data-ttu-id="3178d-103">Regiones de ventana</span><span class="sxs-lookup"><span data-stu-id="3178d-103">Window Regions</span></span>

<span data-ttu-id="3178d-104">Además de la región de actualización, cada ventana tiene un *área visible* que define la parte de la ventana visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="3178d-104">In addition to the update region, every window has a *visible region* that defines the window portion visible to the user.</span></span> <span data-ttu-id="3178d-105">El sistema cambia el área visible de la ventana cada vez que cambia el tamaño de la ventana o cuando se mueve otra ventana de forma que oculta o expone una parte de la ventana.</span><span class="sxs-lookup"><span data-stu-id="3178d-105">The system changes the visible region for the window whenever the window changes size or whenever another window is moved such that it obscures or exposes a portion of the window.</span></span> <span data-ttu-id="3178d-106">Las aplicaciones no pueden cambiar el área visible directamente, pero el sistema utiliza automáticamente el área visible para crear la región de recorte de cualquier contexto de dispositivo de pantalla recuperado para la ventana.</span><span class="sxs-lookup"><span data-stu-id="3178d-106">Applications cannot change the visible region directly, but the system automatically uses the visible region to create the clipping region for any display device context retrieved for the window.</span></span>

<span data-ttu-id="3178d-107">La *región de recorte* determina dónde permite el dibujo el sistema.</span><span class="sxs-lookup"><span data-stu-id="3178d-107">The *clipping region* determines where the system permits drawing.</span></span> <span data-ttu-id="3178d-108">Cuando la aplicación recupera un contexto de dispositivo de pantalla mediante la función [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , el sistema establece la región de recorte para el contexto de dispositivo en la intersección de la región visible y la región de actualización.</span><span class="sxs-lookup"><span data-stu-id="3178d-108">When the application retrieves a display device context using the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc), or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function, the system sets the clipping region for the device context to the intersection of the visible region and the update region.</span></span> <span data-ttu-id="3178d-109">Las aplicaciones pueden cambiar la región de recorte mediante el uso de funciones como [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) y [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), para limitar aún más el dibujo a una parte determinada del área de actualización.</span><span class="sxs-lookup"><span data-stu-id="3178d-109">Applications can change the clipping region by using functions such as [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) and [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), to further limit drawing to a particular portion of the update area.</span></span>

<span data-ttu-id="3178d-110">Los \_ estilos WS CLIPCHILDREN y WS \_ CLIPSIBLINGS especifican el modo en que el sistema calcula el área visible para una ventana.</span><span class="sxs-lookup"><span data-stu-id="3178d-110">The WS\_CLIPCHILDREN and WS\_CLIPSIBLINGS styles further specify how the system calculates the visible region for a window.</span></span> <span data-ttu-id="3178d-111">Si una ventana tiene uno o ambos estilos, el área visible excluye cualquier ventana secundaria o ventanas del mismo nivel (ventanas que tengan la misma ventana primaria).</span><span class="sxs-lookup"><span data-stu-id="3178d-111">If a window has one or both of these styles, the visible region excludes any child window or sibling windows (windows having the same parent window).</span></span> <span data-ttu-id="3178d-112">Por lo tanto, el dibujo que de otro modo informaría en estas ventanas siempre se recortará.</span><span class="sxs-lookup"><span data-stu-id="3178d-112">Therefore, drawing that would otherwise intrude in these windows will always be clipped.</span></span>

 

 



