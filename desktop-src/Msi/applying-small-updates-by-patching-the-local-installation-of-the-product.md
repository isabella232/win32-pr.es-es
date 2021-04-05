---
description: Se puede aplicar una actualización pequeña a una aplicación mediante la aplicación de una revisión de la instalación local de la aplicación.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001747"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="c0e8e-103">Aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto</span><span class="sxs-lookup"><span data-stu-id="c0e8e-103">Applying Small Updates by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="c0e8e-104">Se puede aplicar una actualización pequeña a una aplicación mediante la aplicación de una revisión de la instalación local de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c0e8e-104">A small update can be applied to an application by patching the local installation of the application.</span></span>

<span data-ttu-id="c0e8e-105">**Para aplicar una pequeña revisión de actualización a una instalación local del producto**</span><span class="sxs-lookup"><span data-stu-id="c0e8e-105">**To apply a small update patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="c0e8e-106">Inicie la instalación de la revisión desde la línea de comandos o mediante un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="c0e8e-106">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="c0e8e-107">Para iniciar desde la línea de comandos, use **msiexec/p patch. MSP REINSTALL \[ =**_lista de características_ *_\] REINSTALLMODE = OMUs_*.</span><span class="sxs-lookup"><span data-stu-id="c0e8e-107">To launch from the command line, use **msiexec /p patch.msp REINSTALL=\[**_Feature list_*_\] REINSTALLMODE=omus_*.</span></span> <span data-ttu-id="c0e8e-108">Para iniciar desde un archivo ejecutable, llame a [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o al [**método ApplyPatch**](installer-applypatch.md) y proporcione los mismos argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="c0e8e-108">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="c0e8e-109">Al aplicar una revisión a una instalación de cliente, el instalador omite el origen de instalación y continúa con la revisión de los archivos que ya están instalados en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="c0e8e-109">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="c0e8e-110">El instalador cambia cualquier componente revisado marcado como ejecutar desde el origen a ejecución local.</span><span class="sxs-lookup"><span data-stu-id="c0e8e-110">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="c0e8e-111">Los usuarios no pueden ejecutar estos componentes desde el origen, siempre y cuando la revisión permanezca en el equipo.</span><span class="sxs-lookup"><span data-stu-id="c0e8e-111">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="c0e8e-112">El instalador agrega las transformaciones que se usan para actualizar el archivo. msi o agrega información específica de la revisión al perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="c0e8e-112">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="c0e8e-113">El instalador almacena en caché el archivo. msi en el equipo del usuario para que pueda realizar la instalación a petición, reinstalar y reparar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c0e8e-113">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="c0e8e-114">Después de aplicar una revisión a una instalación independiente, el instalador hace referencia a dos o más listas de origen a archivos externos: una para el origen original y otra para cada revisión que se ha aplicado.</span><span class="sxs-lookup"><span data-stu-id="c0e8e-114">After a patch is applied to a standalone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



