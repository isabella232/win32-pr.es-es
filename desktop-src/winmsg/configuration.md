---
description: En esta sección de referencia se describe la configuración de Windows y mensajes. Obtenga información sobre los elementos de visualización y las métricas del sistema.
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configuración (Windows y mensajes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa516e87aa7d338d4e2fd46a160fcbd6dadb305
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406348"
---
# <a name="configuration-windows-and-messages"></a><span data-ttu-id="5b939-104">Configuración (Windows y mensajes)</span><span class="sxs-lookup"><span data-stu-id="5b939-104">Configuration (Windows and Messages)</span></span>

<span data-ttu-id="5b939-105">*Los elementos de* visualización son las partes de una ventana y la pantalla que aparecen en la pantalla de presentación del sistema.</span><span class="sxs-lookup"><span data-stu-id="5b939-105">*Display elements* are the parts of a window and the display that appear on the system display screen.</span></span> <span data-ttu-id="5b939-106">*Las métricas del* sistema son las dimensiones de varios elementos de presentación.</span><span class="sxs-lookup"><span data-stu-id="5b939-106">*System metrics* are the dimensions of various display elements.</span></span> <span data-ttu-id="5b939-107">Las métricas típicas del sistema incluyen el ancho del borde de la ventana, el alto del icono, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="5b939-107">Typical system metrics include the window border width, icon height, and so on.</span></span> <span data-ttu-id="5b939-108">Las métricas del sistema también describen otros aspectos del sistema, como si se instala un mouse, se admiten caracteres de doble byte o se instala una versión de depuración del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5b939-108">System metrics also describe other aspects of the system, such as whether a mouse is installed, double-byte characters are supported, or a debugging version of the operating system is installed.</span></span> <span data-ttu-id="5b939-109">La [**función GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera la métrica del sistema especificada.</span><span class="sxs-lookup"><span data-stu-id="5b939-109">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function retrieves the specified system metric.</span></span>

<span data-ttu-id="5b939-110">Las aplicaciones también pueden recuperar y establecer el color de los elementos de ventana, como menús, barras de desplazamiento y botones, mediante las funciones [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) y [**SetSysColors,**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5b939-110">Applications can also retrieve and set the color of window elements such as menus, scroll bars, and buttons by using the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) and [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) functions, respectively.</span></span>

<span data-ttu-id="5b939-111">La [**función SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) recupera o establece varios atributos del sistema, como el tiempo de doble clic, el tiempo de espera del protector de pantalla, el ancho del borde de la ventana y el patrón de escritorio.</span><span class="sxs-lookup"><span data-stu-id="5b939-111">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function retrieves or sets various system attributes, such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span> <span data-ttu-id="5b939-112">Cuando una aplicación usa **SystemParametersInfo** para establecer un parámetro, el cambio tiene lugar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5b939-112">When an application uses **SystemParametersInfo** to set a parameter, the change takes place immediately.</span></span> <span data-ttu-id="5b939-113">Esta función también permite que las aplicaciones actualicen el perfil de usuario, por lo que los cambios en el sistema se conservarán cuando se reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="5b939-113">This function also enables applications to update the user profile, so changes to the system will be preserved when the system is restarted.</span></span>

 

 
