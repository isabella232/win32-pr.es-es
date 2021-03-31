---
description: Configuración
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configuración (ventanas y mensajes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac66d2ba25e81582734eb13148d2651b276ea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278628"
---
# <a name="configuration-windows-and-messages"></a><span data-ttu-id="d95a5-103">Configuración (ventanas y mensajes)</span><span class="sxs-lookup"><span data-stu-id="d95a5-103">Configuration (Windows and Messages)</span></span>

<span data-ttu-id="d95a5-104">Los *elementos de visualización* son los elementos de una ventana y la pantalla que aparecen en la pantalla de presentación del sistema.</span><span class="sxs-lookup"><span data-stu-id="d95a5-104">*Display elements* are the parts of a window and the display that appear on the system display screen.</span></span> <span data-ttu-id="d95a5-105">Las *métricas del sistema* son las dimensiones de varios elementos de visualización.</span><span class="sxs-lookup"><span data-stu-id="d95a5-105">*System metrics* are the dimensions of various display elements.</span></span> <span data-ttu-id="d95a5-106">Las métricas típicas del sistema incluyen el ancho del borde de la ventana, el alto del icono, etc.</span><span class="sxs-lookup"><span data-stu-id="d95a5-106">Typical system metrics include the window border width, icon height, and so on.</span></span> <span data-ttu-id="d95a5-107">Las métricas del sistema también describen otros aspectos del sistema, como, por ejemplo, si hay un mouse instalado, se admiten caracteres de doble byte o se instala una versión de depuración del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d95a5-107">System metrics also describe other aspects of the system, such as whether a mouse is installed, double-byte characters are supported, or a debugging version of the operating system is installed.</span></span> <span data-ttu-id="d95a5-108">La función [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera la métrica del sistema especificada.</span><span class="sxs-lookup"><span data-stu-id="d95a5-108">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function retrieves the specified system metric.</span></span>

<span data-ttu-id="d95a5-109">Las aplicaciones también pueden recuperar y establecer el color de los elementos de ventana, como los menús, las barras de desplazamiento y los botones, mediante las funciones [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) y [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d95a5-109">Applications can also retrieve and set the color of window elements such as menus, scroll bars, and buttons by using the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) and [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) functions, respectively.</span></span>

<span data-ttu-id="d95a5-110">La función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) recupera o establece varios atributos del sistema, como el tiempo de doble clic, el tiempo de espera del protector de pantalla, el ancho del borde de la ventana y el patrón de escritorio.</span><span class="sxs-lookup"><span data-stu-id="d95a5-110">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function retrieves or sets various system attributes, such as double-click time, screen saver time-out, window border width, and desktop pattern.</span></span> <span data-ttu-id="d95a5-111">Cuando una aplicación usa **SystemParametersInfo** para establecer un parámetro, el cambio tiene lugar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="d95a5-111">When an application uses **SystemParametersInfo** to set a parameter, the change takes place immediately.</span></span> <span data-ttu-id="d95a5-112">Esta función también permite a las aplicaciones actualizar el perfil de usuario, por lo que los cambios en el sistema se conservarán cuando se reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="d95a5-112">This function also enables applications to update the user profile, so changes to the system will be preserved when the system is restarted.</span></span>

 

 
