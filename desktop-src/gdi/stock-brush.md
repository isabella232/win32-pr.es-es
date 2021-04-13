---
description: La interfaz de dispositivo gráfico (GDI) mantiene siete pinceles de cotización lógica predefinidos. También hay 21 pinceles de cotización lógica predefinidos mantenidos por la interfaz de administración de ventanas (usuario).
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Pincel bursátil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985923"
---
# <a name="stock-brush"></a><span data-ttu-id="070b3-104">Pincel bursátil</span><span class="sxs-lookup"><span data-stu-id="070b3-104">Stock Brush</span></span>

<span data-ttu-id="070b3-105">La interfaz de dispositivo gráfico (GDI) mantiene siete pinceles de cotización lógica predefinidos.</span><span class="sxs-lookup"><span data-stu-id="070b3-105">There are seven predefined logical stock brushes maintained by the graphics device interface (GDI).</span></span> <span data-ttu-id="070b3-106">También hay 21 pinceles de cotización lógica predefinidos mantenidos por la interfaz de administración de ventanas (usuario).</span><span class="sxs-lookup"><span data-stu-id="070b3-106">There are also 21 predefined logical stock brushes maintained by the window management interface (USER).</span></span>

<span data-ttu-id="070b3-107">En la ilustración siguiente se muestran los rectángulos pintados con los siete pinceles de cotización predefinidos.</span><span class="sxs-lookup"><span data-stu-id="070b3-107">The following illustration shows rectangles painted by using the seven predefined stock brushes.</span></span>

![Ilustración que muestra siete cuadros: uno negro, tres tonos de gris y tres que aparecen vacíos](images/csbru-03.png)

<span data-ttu-id="070b3-109">Una aplicación puede recuperar un identificador que identifique uno de los siete pinceles bursátiles mediante una llamada a la función [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) , especificando el tipo de pincel.</span><span class="sxs-lookup"><span data-stu-id="070b3-109">An application can retrieve a handle identifying one of the seven stock brushes by calling the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function, specifying the brush type.</span></span>

<span data-ttu-id="070b3-110">Los 21 pinceles de bolsa que mantiene la interfaz de administración de ventanas se corresponden con los colores de los elementos de ventana, como los menús, las barras de desplazamiento y los botones.</span><span class="sxs-lookup"><span data-stu-id="070b3-110">The 21 stock brushes maintained by the window management interface correspond to the colors of window elements such as menus, scroll bars, and buttons.</span></span> <span data-ttu-id="070b3-111">Una aplicación puede obtener un identificador que identifique uno de estos pinceles llamando a la función [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) y especificando un valor de color del sistema.</span><span class="sxs-lookup"><span data-stu-id="070b3-111">An application can obtain a handle identifying one of these brushes by calling the [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) function and specifying a system-color value.</span></span> <span data-ttu-id="070b3-112">Una aplicación puede recuperar el color correspondiente a un elemento de ventana determinado mediante una llamada a la función [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) .</span><span class="sxs-lookup"><span data-stu-id="070b3-112">An application can retrieve the color corresponding to a particular window element by calling the [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) function.</span></span> <span data-ttu-id="070b3-113">Una aplicación puede establecer el color correspondiente a un elemento de ventana mediante una llamada a la función [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) .</span><span class="sxs-lookup"><span data-stu-id="070b3-113">An application can set the color corresponding to a window element by calling the [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) function.</span></span>

 

 
