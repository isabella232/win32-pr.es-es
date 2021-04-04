---
title: Redistribuir Windows Media Player serie 9
description: Redistribuir Windows Media Player serie 9
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076265"
---
# <a name="redistributing-windows-media-player-9-series"></a><span data-ttu-id="156f3-103">Redistribuir Windows Media Player serie 9</span><span class="sxs-lookup"><span data-stu-id="156f3-103">Redistributing Windows Media Player 9 Series</span></span>

<span data-ttu-id="156f3-104">Puede instalar Windows Media Player 9 series en Windows XP con uno de los siguientes programas de instalación.</span><span class="sxs-lookup"><span data-stu-id="156f3-104">You can install Windows Media Player 9 Series on Windows XP by using one of the following setup programs.</span></span>

-   <span data-ttu-id="156f3-105">MPSetupXP.exe</span><span class="sxs-lookup"><span data-stu-id="156f3-105">MPSetupXP.exe</span></span>
-   <span data-ttu-id="156f3-106">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="156f3-106">MPSetup.exe</span></span>

> [!Note]  
> <span data-ttu-id="156f3-107">MPSetup.exe es un superconjunto del programa de instalación de MPSetupXP.exe.</span><span class="sxs-lookup"><span data-stu-id="156f3-107">MPSetup.exe is a superset of the MPSetupXP.exe setup program.</span></span> <span data-ttu-id="156f3-108">Contiene archivos que son necesarios para los sistemas operativos publicados antes de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="156f3-108">It contains files that are needed by operating systems released before Windows XP.</span></span> <span data-ttu-id="156f3-109">MPSetup.exe es funcionalmente equivalente a MPSetupXP.exe cuando se ejecuta en Windows XP, pero el tamaño del archivo del programa de instalación es mayor porque no se ha optimizado para la instalación en los sistemas operativos Windows XP.</span><span class="sxs-lookup"><span data-stu-id="156f3-109">MPSetup.exe is functionally equivalent to MPSetupXP.exe when run on Windows XP, but the setup program file size is larger because it has not been optimized for installation on Windows XP operating systems.</span></span>

 

<span data-ttu-id="156f3-110">Puede instalar Windows Media Player 9 series en Windows 98 Second Edition, Windows Millennium Edition o Windows 2000 con el siguiente programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="156f3-110">You can install Windows Media Player 9 Series on Windows 98 Second Edition, Windows Millennium Edition or Windows 2000 by using the following setup program.</span></span>

-   <span data-ttu-id="156f3-111">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="156f3-111">MPSetup.exe</span></span>

<span data-ttu-id="156f3-112">Este es un ejemplo de una línea de comandos para la instalación sin interfaz de usuario y sin solicitud de reinicio o reinicio.</span><span class="sxs-lookup"><span data-stu-id="156f3-112">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> <span data-ttu-id="156f3-113">El parámetro/P: \# e especifica que el paquete de instalación de windows media Player debe almacenarse en la memoria caché durante el programa de instalación de windows media Player.</span><span class="sxs-lookup"><span data-stu-id="156f3-113">The /P:\#e parameter specifies that the Windows Media Player installation package should be cached during Windows Media Player setup.</span></span> <span data-ttu-id="156f3-114">Este comando se utiliza para controlar las actualizaciones futuras del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="156f3-114">This command is used to handle future upgrades of the operating system.</span></span> <span data-ttu-id="156f3-115">Este comando solo lo deben omitir los administradores de TI corporativos.</span><span class="sxs-lookup"><span data-stu-id="156f3-115">This command should be omitted only by corporate IT administrators.</span></span> <span data-ttu-id="156f3-116">El único caso en el que/P: \# e no debe incluirse en la línea de comandos es cuando es el propietario del sistema de destino y sabe que el sistema de destino nunca se actualizará a un sistema operativo posterior.</span><span class="sxs-lookup"><span data-stu-id="156f3-116">The only case where /P:\#e should not be included on the command line is when you own the target system and know that the target system will never be upgraded to a later operating system.</span></span> <span data-ttu-id="156f3-117">Por ejemplo, si va a instalar Windows Media Player 9 series en Windows 2000 y el equipo puede actualizarse algún día a Windows XP, debe usar/P: \# e en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="156f3-117">For example, if you are installing Windows Media Player 9 Series on Windows 2000 and the computer may someday be upgraded to Windows XP, you must use /P:\#e on the command line.</span></span> <span data-ttu-id="156f3-118">De lo contrario, después de la instalación de Windows XP, los archivos de Windows Media Player se sobrescribirán con los archivos de Windows Media Player para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="156f3-118">Otherwise, after the Windows XP installation, the Windows Media Player files will be overwritten with the files for Windows Media Player for Windows XP.</span></span>

 

<span data-ttu-id="156f3-119">En la tabla siguiente se muestran parámetros adicionales que puede usar con el programa de instalación de Windows Media Player 9 series.</span><span class="sxs-lookup"><span data-stu-id="156f3-119">The following table shows additional parameters that you can use with the Windows Media Player 9 Series setup program.</span></span>



| <span data-ttu-id="156f3-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="156f3-120">Parameter</span></span>              | <span data-ttu-id="156f3-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="156f3-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="156f3-122">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="156f3-122">/NoMigrate</span></span>             | <span data-ttu-id="156f3-123">Impedir la migración de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="156f3-123">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="156f3-124">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="156f3-124">/NestedRestore</span></span>         | <span data-ttu-id="156f3-125">Cree un punto de restauración del sistema anidado.</span><span class="sxs-lookup"><span data-stu-id="156f3-125">Create a nested system restore point.</span></span> <span data-ttu-id="156f3-126">Úselo si la aplicación crea un punto de restauración del sistema para anidar el punto de restauración de Windows Media Player en el punto de restauración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="156f3-126">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="156f3-127">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="156f3-127">/DisallowSystemRestore</span></span> | <span data-ttu-id="156f3-128">No permitir la creación de un punto de restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="156f3-128">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="156f3-129">Esta marca deshabilitará la creación de un punto de restauración del sistema.</span><span class="sxs-lookup"><span data-stu-id="156f3-129">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="156f3-130">En la mayoría de los casos, esta marca no debe usarse para la redistribución de software general.</span><span class="sxs-lookup"><span data-stu-id="156f3-130">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="156f3-131">Esto solo debe usarse cuando se puede realizar una elección explícita en nombre del usuario final para no admitir la reversión de los archivos de Windows Media Player a una versión anterior del reproductor.</span><span class="sxs-lookup"><span data-stu-id="156f3-131">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="156f3-132">Esta marca solo se debe usar para la instalación corporativa o la instalación del fabricante de equipos originales (OEM).</span><span class="sxs-lookup"><span data-stu-id="156f3-132">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |



 

## <a name="notes"></a><span data-ttu-id="156f3-133">Notas</span><span class="sxs-lookup"><span data-stu-id="156f3-133">Notes</span></span>

-   <span data-ttu-id="156f3-134">Los parámetros de la línea de comandos distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="156f3-134">The command-line parameters are case-sensitive.</span></span>
-   <span data-ttu-id="156f3-135">Al suprimir el mensaje de reinicio, debe comprobar la clave del registro InstallResult y controlar la notificación de reinicio en la aplicación de instalación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="156f3-135">When suppressing the restart prompt, you must check the InstallResult registry key and handle restart notification in the calling setup application.</span></span>
-   <span data-ttu-id="156f3-136">Windows Media Player 9 series también instala Windows Media Format en tiempo de ejecución, por lo que no es necesario incluir el paquete de distribución de Windows Media Player y el paquete de distribución en tiempo de ejecución de Windows Media Format en el mismo paquete de distribución de software.</span><span class="sxs-lookup"><span data-stu-id="156f3-136">Windows Media Player 9 Series also installs the Windows Media Format runtime, so there is no need to include both the Windows Media Player distribution package and the Windows Media Format runtime distribution package in the same software redistribution package.</span></span> <span data-ttu-id="156f3-137">Por lo tanto, si incluye MPSetup.exe o MPSetupXP.exe en su instalación, no es necesario incluir WMFdist.exe.</span><span class="sxs-lookup"><span data-stu-id="156f3-137">Therefore, if you include MPSetup.exe or MPSetupXP.exe in your installation, you do not need to include WMFdist.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="156f3-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="156f3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="156f3-139">**Redistribuir el software de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="156f3-139">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




