---
description: Una aplicación realiza pruebas de posicionamiento en regiones para determinar las coordenadas de la posición actual del cursor.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Regiones de pruebas de posicionamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276003"
---
# <a name="hit-testing-regions"></a><span data-ttu-id="6ae1a-103">Regiones de pruebas de posicionamiento</span><span class="sxs-lookup"><span data-stu-id="6ae1a-103">Hit Testing Regions</span></span>

<span data-ttu-id="6ae1a-104">Una aplicación realiza pruebas de posicionamiento en regiones para determinar las coordenadas de la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-104">An application performs hit testing on regions to determine the coordinates of the current cursor position.</span></span> <span data-ttu-id="6ae1a-105">Después, pasa estas coordenadas, así como un identificador que identifica la región en la función [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) .</span><span class="sxs-lookup"><span data-stu-id="6ae1a-105">Then it passes these coordinates as well as a handle identifying the region to the [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) function.</span></span> <span data-ttu-id="6ae1a-106">Las coordenadas del cursor se pueden recuperar procesando los diversos mensajes del mouse, [**como \_ WM LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) y [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md).</span><span class="sxs-lookup"><span data-stu-id="6ae1a-106">The cursor coordinates can be retrieved by processing the various mouse messages, such as [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) , [**WM\_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) , and [**WM\_RBUTTONUP**](../inputdev/wm-rbuttonup.md).</span></span> <span data-ttu-id="6ae1a-107">El valor devuelto para PtInRegion indica si la posición del cursor está dentro de la región especificada.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-107">The return value for PtInRegion indicates whether the cursor position is within the given region.</span></span>

 

 
