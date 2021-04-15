---
title: Restaurar el sistema
description: A medida que el equipo se usa a lo largo del tiempo, los puntos de restauración se recopilan en el archivo de datos sin necesidad de administración o intervención requerida por el usuario.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c5ff4aef88ec9eca591ee3c1afb1ad570689a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695318"
---
# <a name="restoring-the-system"></a><span data-ttu-id="cbf7c-103">Restaurar el sistema</span><span class="sxs-lookup"><span data-stu-id="cbf7c-103">Restoring the System</span></span>

<span data-ttu-id="cbf7c-104">A medida que el equipo se usa a lo largo del tiempo, los puntos de restauración se recopilan en el archivo de datos sin necesidad de administración o intervención requerida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-104">As the computer is used over time, restore points are collected in the data archive without any management or intervention required by the user.</span></span> <span data-ttu-id="cbf7c-105">Si el usuario necesita restaurar el sistema a un estado anterior, los puntos de restauración disponibles se hacen visibles al usuario a través de la interfaz de usuario de restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-105">If the user ever needs to restore the system to a previous state, the available restore points are made visible to the user through the System Restore user interface.</span></span> <span data-ttu-id="cbf7c-106">El usuario puede elegir cualquiera de estos puntos de restauración.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-106">The user can choose any of these restore points.</span></span> <span data-ttu-id="cbf7c-107">La única manera de tener acceso a este archivo de puntos de restauración es a través de la interfaz de usuario de restauración del sistema y la API de restauración del sistema. Esto se hace para proteger la integridad de los datos y evitar cambios accidentales realizados por el usuario, las aplicaciones u otros agentes.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-107">The only way to access this archive of restore points is through the System Restore user interface and the System Restore API; this is to protect data integrity and prevent accidental changes made by the user, applications, or other agents.</span></span>

<span data-ttu-id="cbf7c-108">Para restaurar un sistema, Restaurar sistema deshace los cambios de archivo realizados en los archivos supervisados, recapturando el estado del archivo en el momento del punto de restauración seleccionado.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-108">To restore a system, System Restore undoes file changes made to monitored files, recapturing the file state at the time of the selected restore point.</span></span> <span data-ttu-id="cbf7c-109">A continuación, reemplaza el registro actual por el que se guardó para el punto de restauración seleccionado.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-109">It then replaces the current registry with the one saved for the selected restore point.</span></span>

<span data-ttu-id="cbf7c-110">Para asegurarse de que la aplicación tenga el comportamiento deseado después de una restauración, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbf7c-110">To ensure that your application has the desired behavior after a restore, do the following:</span></span>

-   <span data-ttu-id="cbf7c-111">No almacene información en el registro que impida el acceso de los usuarios a archivos de datos personales o a aplicaciones en Restaurar sistema.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-111">Do not store information in the registry that prevents user access to personal data files or applications on system restore.</span></span> <span data-ttu-id="cbf7c-112">De lo contrario, debe proporcionar un mecanismo por el que el usuario pueda descargar y volver a instalar las aplicaciones sin tener que pagarlas de nuevo.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-112">Otherwise, you must provide a mechanism by which the user can download and reinstall the applications without having to pay for them again.</span></span>
-   <span data-ttu-id="cbf7c-113">Use la [API de restauración del sistema](system-restore-api.md) para crear puntos de restauración significativos en instalación y desinstalación.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-113">Use the [System Restore API](system-restore-api.md) to create meaningful restore points at install and uninstall.</span></span>
-   <span data-ttu-id="cbf7c-114">En Windows XP, los archivos binarios de la aplicación clave que se van a proteger deben usar extensiones coherentes con las utilizadas en Filelist.xml.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-114">In Windows XP, the key application binaries to be protected must use extensions consistent with those used in Filelist.xml.</span></span> <span data-ttu-id="cbf7c-115">Para obtener más información, vea [extensiones de nombre de archivo supervisado](monitored-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="cbf7c-115">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span> <span data-ttu-id="cbf7c-116">Windows 7 y Windows Vista no usan este archivo.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-116">This file is not used by Windows 7 and Windows Vista.</span></span> <span data-ttu-id="cbf7c-117">No use tipos de extensión supervisados para archivos editables por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-117">Do not use monitored extension types for user-editable files.</span></span> <span data-ttu-id="cbf7c-118">Por ejemplo, si se denomina el archivo de datos personales de un usuario mediante la extensión. ini, el usuario puede perder el trabajo como resultado de una restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="cbf7c-118">For example, if you name a user's personal data file using the extension .ini, the user may lose work as a result of a system restore.</span></span>

 

 




