---
title: Estaciones de ventana
description: Una estación de ventana contiene un portapapeles, una tabla Atom y uno o más objetos de escritorio. Cada objeto de estación de ventana es un objeto protegible. Cuando se crea una estación de ventana, se asocia al proceso de llamada y se asigna a la sesión actual.
ms.assetid: 617661e2-3b0d-42a9-9769-2ba0957c31a8
keywords:
- objetos de la estación de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2048015e4b0c687932c4d01aafe31127e2141e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077924"
---
# <a name="window-stations"></a><span data-ttu-id="d9b0b-106">Estaciones de ventana</span><span class="sxs-lookup"><span data-stu-id="d9b0b-106">Window Stations</span></span>

<span data-ttu-id="d9b0b-107">Una *estación de ventana* contiene un portapapeles, una tabla Atom y uno o más objetos de [escritorio](desktops.md) .</span><span class="sxs-lookup"><span data-stu-id="d9b0b-107">A *window station* contains a clipboard, an atom table, and one or more [desktop](desktops.md) objects.</span></span> <span data-ttu-id="d9b0b-108">Cada objeto de estación de ventana es un objeto protegible.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-108">Each window station object is a securable object.</span></span> <span data-ttu-id="d9b0b-109">Cuando se crea una estación de ventana, se asocia al proceso de llamada y se asigna a la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-109">When a window station is created, it is associated with the calling process and assigned to the current session.</span></span>

<span data-ttu-id="d9b0b-110">La *estación de ventana interactiva* es la única estación de ventana que puede mostrar una interfaz de usuario o recibir datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-110">The *interactive window station* is the only window station that can display a user interface or receive user input.</span></span> <span data-ttu-id="d9b0b-111">Se asigna a la sesión de inicio de sesión del usuario interactivo y contiene el teclado, el mouse y el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-111">It is assigned to the logon session of the interactive user, and contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="d9b0b-112">Siempre se denomina "WinSta0".</span><span class="sxs-lookup"><span data-stu-id="d9b0b-112">It is always named "WinSta0".</span></span> <span data-ttu-id="d9b0b-113">El resto de las estaciones de ventana no son interactivas, lo que significa que no pueden mostrar una interfaz de usuario ni recibir datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-113">All other window stations are noninteractive, which means they cannot display a user interface or receive user input.</span></span>

<span data-ttu-id="d9b0b-114">Cuando un usuario inicia sesión en un equipo mediante Servicios de Escritorio remoto, se inicia una sesión para el usuario.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-114">When a user logs on to a computer using Remote Desktop Services, a session is started for the user.</span></span> <span data-ttu-id="d9b0b-115">Cada sesión está asociada a su propia estación de ventana interactiva denominada "WinSta0".</span><span class="sxs-lookup"><span data-stu-id="d9b0b-115">Each session is associated with its own interactive window station named "WinSta0".</span></span> <span data-ttu-id="d9b0b-116">Para obtener más información, vea [sesiones de escritorio remoto](/windows/desktop/TermServ/terminal-services-sessions).</span><span class="sxs-lookup"><span data-stu-id="d9b0b-116">For more information, see [Remote Desktop Sessions](/windows/desktop/TermServ/terminal-services-sessions).</span></span>

<span data-ttu-id="d9b0b-117">Para obtener más información sobre las estaciones de ventana, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="d9b0b-117">For more information on window stations, see the following topics:</span></span>

-   [<span data-ttu-id="d9b0b-118">Creación de estación de ventana y escritorio</span><span class="sxs-lookup"><span data-stu-id="d9b0b-118">Window Station and Desktop Creation</span></span>](window-station-and-desktop-creation.md)
-   [<span data-ttu-id="d9b0b-119">Proceso de conexión a una estación de ventana</span><span class="sxs-lookup"><span data-stu-id="d9b0b-119">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
-   [<span data-ttu-id="d9b0b-120">Seguridad y derechos de acceso de la estación de ventana</span><span class="sxs-lookup"><span data-stu-id="d9b0b-120">Window Station Security and Access Rights</span></span>](window-station-security-and-access-rights.md)

 

 