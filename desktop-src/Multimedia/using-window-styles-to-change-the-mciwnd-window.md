---
title: Usar estilos de ventana para cambiar la ventana de MCIWnd
description: Usar estilos de ventana para cambiar la ventana de MCIWnd
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- MCIWndCreate función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665791"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a><span data-ttu-id="18cd3-104">Usar estilos de ventana para cambiar la ventana de MCIWnd</span><span class="sxs-lookup"><span data-stu-id="18cd3-104">Using Window Styles to Change the MCIWnd Window</span></span>

<span data-ttu-id="18cd3-105">Como ocurre con cualquier ventana, puede cambiar la apariencia y el comportamiento de una ventana de MCIWnd eligiendo entre los estilos de ventana estándar especificados con la función [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="18cd3-105">As with any window, you can change the appearance and behavior of an MCIWnd window by choosing from the standard window styles specified with the [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="18cd3-106">Además, puede elegir entre otros estilos de ventana específicos de MCIWnd Windows.</span><span class="sxs-lookup"><span data-stu-id="18cd3-106">In addition, you can choose from several other window styles that are specific to MCIWnd windows.</span></span> <span data-ttu-id="18cd3-107">Con estos estilos, la aplicación puede cambiar estas ventanas MCIWnd de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="18cd3-107">With these styles, your application can change these MCIWnd windows in the following ways:</span></span>

-   <span data-ttu-id="18cd3-108">Cambiar el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="18cd3-108">Change window size.</span></span>
-   <span data-ttu-id="18cd3-109">Ocultar o mostrar controles.</span><span class="sxs-lookup"><span data-stu-id="18cd3-109">Hide or display controls.</span></span>
-   <span data-ttu-id="18cd3-110">Emitir mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="18cd3-110">Issue notification messages.</span></span>
-   <span data-ttu-id="18cd3-111">Mostrar información en la barra de título.</span><span class="sxs-lookup"><span data-stu-id="18cd3-111">Display information in the title bar.</span></span>

<span data-ttu-id="18cd3-112">Puede establecer estilos de ventana mediante su especificación en la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) , o bien puede usar la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) para cambiar el estilo de una ventana MCIWnd existente.</span><span class="sxs-lookup"><span data-stu-id="18cd3-112">You can set window styles by specifying them in the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function, or you can use the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro to change the style of an existing MCIWnd window.</span></span> <span data-ttu-id="18cd3-113">También puede consultar una ventana de MCIWnd para obtener sus estilos actuales mediante la macro [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) .</span><span class="sxs-lookup"><span data-stu-id="18cd3-113">You can also query an MCIWnd window for its current styles by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>

<span data-ttu-id="18cd3-114">Para obtener una lista de los estilos de ventana específicos de MCIWnd, vea [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span><span class="sxs-lookup"><span data-stu-id="18cd3-114">For a list of the MCIWnd-specific window styles, see [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span>

 

 