---
description: 'Las aplicaciones de Direct3D pueden ejecutarse en cualquiera de los dos modos: pantalla completa o con ventanas.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Modo de ventana de vs Full-Screen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf51c641446d3f54ceb37c9cc1ac629604f68400
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152112"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a><span data-ttu-id="b045b-103">Modo de ventana de vs Full-Screen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b045b-103">Windowed vs Full-Screen Mode (Direct3D 9)</span></span>

<span data-ttu-id="b045b-104">Las aplicaciones de Direct3D pueden ejecutarse en cualquiera de los dos modos: pantalla completa o con ventanas.</span><span class="sxs-lookup"><span data-stu-id="b045b-104">Direct3D applications can run in either of two modes: full-screen or windowed.</span></span>

<span data-ttu-id="b045b-105">El modo de pantalla completa significa que la ventana en la que se ejecuta la aplicación abarca todo el escritorio, ocultando todas las aplicaciones en ejecución (incluido el entorno de desarrollo).</span><span class="sxs-lookup"><span data-stu-id="b045b-105">Full-screen mode means the window that the application runs in covers the entire desktop, hiding all running applications (including your development environment).</span></span> <span data-ttu-id="b045b-106">Normalmente, los juegos tienen como valor predeterminado el modo de pantalla completa para sumergir completamente al usuario en el juego ocultando todas las aplicaciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="b045b-106">Games typically default to full-screen mode to fully immerse the user in the game by hiding all running applications.</span></span> <span data-ttu-id="b045b-107">Una aplicación que se ejecuta en modo de ventana comparte el escritorio con todas las aplicaciones en ejecución.</span><span class="sxs-lookup"><span data-stu-id="b045b-107">An application running in windowed-mode shares the desktop with all running applications.</span></span> <span data-ttu-id="b045b-108">Las diferencias de código entre el modo de pantalla completa y el modo de ventana son muy pequeñas.</span><span class="sxs-lookup"><span data-stu-id="b045b-108">Code differences between full-screen mode and windowed mode are very small.</span></span>

<span data-ttu-id="b045b-109">Dado que una aplicación que se ejecuta en el modo de pantalla completa ocupa la pantalla, la depuración de la aplicación requiere un monitor independiente o el uso de un depurador remoto.</span><span class="sxs-lookup"><span data-stu-id="b045b-109">Because an application running in full-screen mode takes over the screen, debugging the application requires either a separate monitor or the use of a remote debugger.</span></span> <span data-ttu-id="b045b-110">Use la [herramienta panel de control de DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) para habilitar la depuración de varios monitores.</span><span class="sxs-lookup"><span data-stu-id="b045b-110">Use the [DirectX Control Panel Tool](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) to enable multiple-monitor debugging.</span></span> <span data-ttu-id="b045b-111">Una de las ventajas de una aplicación en modo de ventana es que puede recorrer paso a paso el código en un depurador sin varios monitores o un depurador remoto.</span><span class="sxs-lookup"><span data-stu-id="b045b-111">One advantage of a windowed-mode application is that you can step through the code in a debugger without multiple monitors or a remote debugger.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b045b-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b045b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b045b-113">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="b045b-113">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 



