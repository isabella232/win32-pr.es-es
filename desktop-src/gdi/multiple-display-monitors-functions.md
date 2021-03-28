---
description: Las funciones siguientes proporcionan compatibilidad con varios monitores.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Múltiples funciones de monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984927"
---
# <a name="multiple-display-monitors-functions"></a><span data-ttu-id="4a4e0-103">Múltiples funciones de monitores de pantalla</span><span class="sxs-lookup"><span data-stu-id="4a4e0-103">Multiple Display Monitors Functions</span></span>

<span data-ttu-id="4a4e0-104">Las funciones siguientes proporcionan compatibilidad con varios monitores.</span><span class="sxs-lookup"><span data-stu-id="4a4e0-104">The following functions provide support for multiple monitors.</span></span>



| <span data-ttu-id="4a4e0-105">Función</span><span class="sxs-lookup"><span data-stu-id="4a4e0-105">Function</span></span>                                           | <span data-ttu-id="4a4e0-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a4e0-106">Description</span></span>                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a4e0-107">**EnumDisplayMonitors**</span><span class="sxs-lookup"><span data-stu-id="4a4e0-107">**EnumDisplayMonitors**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | <span data-ttu-id="4a4e0-108">Enumera los monitores de visualización que intersecan una región formada por la intersección de un rectángulo de recorte especificado y el área visible de un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a4e0-108">Enumerates display monitors that intersect a region formed by the intersection of a specified clipping rectangle and the visible region of a device context.</span></span> |
| [<span data-ttu-id="4a4e0-109">**GetMonitorInfo**</span><span class="sxs-lookup"><span data-stu-id="4a4e0-109">**GetMonitorInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | <span data-ttu-id="4a4e0-110">Recupera información acerca de un monitor de pantalla.</span><span class="sxs-lookup"><span data-stu-id="4a4e0-110">Retrieves information about a display monitor.</span></span>                                                                                                               |
| [<span data-ttu-id="4a4e0-111">**MonitorEnumProc**</span><span class="sxs-lookup"><span data-stu-id="4a4e0-111">**MonitorEnumProc**</span></span>](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | <span data-ttu-id="4a4e0-112">Función de devolución de llamada definida por la aplicación a la que llama la función [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .</span><span class="sxs-lookup"><span data-stu-id="4a4e0-112">An application-defined callback function that is called by the [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) function.</span></span>                                  |
| [<span data-ttu-id="4a4e0-113">**MonitorFromPoint**</span><span class="sxs-lookup"><span data-stu-id="4a4e0-113">**MonitorFromPoint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | <span data-ttu-id="4a4e0-114">Recupera un identificador para el monitor de pantalla que contiene un punto especificado.</span><span class="sxs-lookup"><span data-stu-id="4a4e0-114">Retrieves a handle to the display monitor that contains a specified point.</span></span>                                                                                   |
| [<span data-ttu-id="4a4e0-115">**MonitorFromRect**</span><span class="sxs-lookup"><span data-stu-id="4a4e0-115">**MonitorFromRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | <span data-ttu-id="4a4e0-116">Recupera un identificador para el monitor de pantalla que tiene el área más grande de intersección con un rectángulo especificado.</span><span class="sxs-lookup"><span data-stu-id="4a4e0-116">Retrieves a handle to the display monitor that has the largest area of intersection with a specified rectangle.</span></span>                                              |
| [<span data-ttu-id="4a4e0-117">**MonitorFromWindow**</span><span class="sxs-lookup"><span data-stu-id="4a4e0-117">**MonitorFromWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | <span data-ttu-id="4a4e0-118">Recupera un identificador para el monitor de pantalla que tiene el área más grande de intersección con el rectángulo delimitador de una ventana especificada.</span><span class="sxs-lookup"><span data-stu-id="4a4e0-118">Retrieves a handle to the display monitor that has the largest area of intersection with the bounding rectangle of a specified window.</span></span>                       |



 

 

 



