---
description: El directorio de Windows es el directorio que contiene las aplicaciones basadas en Windows, los archivos de inicialización y los archivos de ayuda. La función GetWindowsDirectory recupera la ruta de acceso a este directorio.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Configuración del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38aa2c2b6b4f6b3ac5caac78a89ad980a9bd074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277952"
---
# <a name="operating-system-configuration"></a><span data-ttu-id="d1c08-104">Configuración del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d1c08-104">Operating System Configuration</span></span>

<span data-ttu-id="d1c08-105">El *Directorio de Windows* es el directorio que contiene las aplicaciones basadas en Windows, los archivos de inicialización y los archivos de ayuda.</span><span class="sxs-lookup"><span data-stu-id="d1c08-105">The *Windows directory* is the directory that contains Windows-based applications, initialization files, and help files.</span></span> <span data-ttu-id="d1c08-106">La función [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) recupera la ruta de acceso a este directorio.</span><span class="sxs-lookup"><span data-stu-id="d1c08-106">The [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="d1c08-107">El *directorio del sistema* es el directorio que contiene las bibliotecas de vínculos dinámicos, los controladores y los archivos de fuentes.</span><span class="sxs-lookup"><span data-stu-id="d1c08-107">The *system directory* is the directory that contains dynamic-link libraries, drivers, and font files.</span></span> <span data-ttu-id="d1c08-108">La función [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) recupera la ruta de acceso a este directorio.</span><span class="sxs-lookup"><span data-stu-id="d1c08-108">The [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) function retrieves the path to this directory.</span></span>

<span data-ttu-id="d1c08-109">La función [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) recupera el nombre del usuario que ha iniciado sesión actualmente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="d1c08-109">The [**GetUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) function retrieves the name of the user currently logged onto the system.</span></span> <span data-ttu-id="d1c08-110">El nombre de usuario es el nombre de inicio de sesión o el nombre completo del usuario, si este último se incluye en el registro.</span><span class="sxs-lookup"><span data-stu-id="d1c08-110">The user name is either the logon name or the user's full name, if the latter is included in the registry.</span></span>

<span data-ttu-id="d1c08-111">Una *variable de entorno* es una variable simbólica que representa algún elemento del sistema, como una ruta de acceso, un nombre de archivo u otros datos literales.</span><span class="sxs-lookup"><span data-stu-id="d1c08-111">An *environment variable* is a symbolic variable that represents some element of the system, such as a path, a file name, or other literal data.</span></span> <span data-ttu-id="d1c08-112">Por ejemplo, la variable de entorno PATH representa los directorios en los que buscar archivos ejecutables.</span><span class="sxs-lookup"><span data-stu-id="d1c08-112">For example, the environment variable PATH represents the directories in which to search for executable files.</span></span> <span data-ttu-id="d1c08-113">Cuando un usuario inicia sesión, el sistema inicializa las variables de entorno en función de la sección de entorno del registro.</span><span class="sxs-lookup"><span data-stu-id="d1c08-113">When a user logs on, the system initializes environment variables based on the environment section of the registry.</span></span> <span data-ttu-id="d1c08-114">La función [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) recupera los valores de las variables de entorno especificadas.</span><span class="sxs-lookup"><span data-stu-id="d1c08-114">The [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) function retrieves the values of specified environment variables.</span></span>

<span data-ttu-id="d1c08-115">La interfaz [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) proporciona información adicional.</span><span class="sxs-lookup"><span data-stu-id="d1c08-115">Additional information is provided by the [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) interface.</span></span>

 

 
