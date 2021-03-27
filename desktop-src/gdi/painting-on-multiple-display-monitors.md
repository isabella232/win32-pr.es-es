---
description: El sistema controla automáticamente el dibujo en un contexto de dispositivo (DC) que abarca más de un monitor, incluso cuando los monitores tienen diferentes profundidades de color.
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: Pintar en varios monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b6a3e3699000399c61e641137a951ed321fd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811906"
---
# <a name="painting-on-multiple-display-monitors"></a><span data-ttu-id="c60de-103">Pintar en varios monitores de pantalla</span><span class="sxs-lookup"><span data-stu-id="c60de-103">Painting on Multiple Display Monitors</span></span>

<span data-ttu-id="c60de-104">El sistema controla automáticamente el dibujo en un contexto de dispositivo (DC) que abarca más de un monitor, incluso cuando los monitores tienen diferentes profundidades de color.</span><span class="sxs-lookup"><span data-stu-id="c60de-104">The system automatically handles painting into a device context (DC) that spans more than one monitor, even when the monitors have different color depths.</span></span> <span data-ttu-id="c60de-105">Normalmente, esto produce buenos resultados, pero puede no ser óptimo.</span><span class="sxs-lookup"><span data-stu-id="c60de-105">Usually this produces good results, but it may not be optimal.</span></span> <span data-ttu-id="c60de-106">Por ejemplo, una ventana de dos monitores de profundidades de color considerablemente diferentes podría tener una representación de color deficiente.</span><span class="sxs-lookup"><span data-stu-id="c60de-106">For example, a window on two monitors of vastly different color depths could have poor color rendition.</span></span> <span data-ttu-id="c60de-107">Además, los monitores con la misma profundidad de color pueden tener un ejemplo de formatsfor de color diferente, los colores se pueden codificar con diferentes números de bits o estar ubicados en lugares diferentes en el valor de color de un píxel.</span><span class="sxs-lookup"><span data-stu-id="c60de-107">Also, monitors with the same color depth may have different color formatsfor example, colors could be encoded with different numbers of bits, or be located in different places in a pixel's color value.</span></span>

<span data-ttu-id="c60de-108">Para obtener los mejores resultados de cada uno de los monitores de un controlador de dominio que abarca más de una pantalla, llame a [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) para enumerar los monitores que forman una intersección con el controlador de dominio y pinte el área de intersección de cada uno de ellos por separado según los atributos de visualización de ese monitor.</span><span class="sxs-lookup"><span data-stu-id="c60de-108">To get the best results for each of the monitors in a DC that spans more than one display, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) to enumerate the monitors that intersect your DC and paint the intersecting area in each of them separately according to the display attributes for that monitor.</span></span> <span data-ttu-id="c60de-109">Vea el ejemplo del [dibujo en un controlador de dominio que abarca varias pantallas](painting-on-a-dc-that-spans-multiple-displays.md).</span><span class="sxs-lookup"><span data-stu-id="c60de-109">See the example in [Painting on a DC That Spans Multiple Displays](painting-on-a-dc-that-spans-multiple-displays.md).</span></span>

<span data-ttu-id="c60de-110">Si realiza todo el dibujo en el código de **\_ Paint de WM** y el código de **\_ Paint de WM** controla todos los distintos modos de vídeo, debería poder colocar el código de la **\_ pintura de WM** en el **MonitorEnumProc** de [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) con solo algunas modificaciones.</span><span class="sxs-lookup"><span data-stu-id="c60de-110">If you do all of your drawing in your **WM\_PAINT** code and if your **WM\_PAINT** code handles all of the various video modes, then you should be able to place your **WM\_PAINT** code in the **MonitorEnumProc** of [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) with only a few modifications.</span></span>

 

 



