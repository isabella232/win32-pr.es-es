---
description: Una actualización principal se puede aplicar a una aplicación si se aplica una revisión a la instalación local de la aplicación desde la línea de comandos o mediante un archivo ejecutable.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Aplicar las actualizaciones principales mediante la revisión de la instalación local del producto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909101"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a><span data-ttu-id="c4e8b-103">Aplicar las actualizaciones principales mediante la revisión de la instalación local del producto</span><span class="sxs-lookup"><span data-stu-id="c4e8b-103">Applying Major Upgrades by Patching the Local Installation of the Product</span></span>

<span data-ttu-id="c4e8b-104">Una actualización principal se puede aplicar a una aplicación si se aplica una revisión a la instalación local de la aplicación desde la línea de comandos o mediante un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="c4e8b-104">A major upgrade can be applied to an application by patching the local installation of the application from the command line or by using an executable.</span></span>

> [!Note]  
> <span data-ttu-id="c4e8b-105">No se recomienda proporcionar una actualización principal como paquete de revisión porque un paquete de revisión de actualización principal no se puede secuenciar con otras actualizaciones y porque la revisión no es una [revisión desinstalable](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="c4e8b-105">Providing a major upgrade as a patch package is not recommended because a major upgrade patch package cannot be sequenced with other updates and because the patch is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="c4e8b-106">La utilidad de [Msimsp.exe](msimsp-exe.md) no se puede usar para generar un paquete de revisión que aplique una actualización principal.</span><span class="sxs-lookup"><span data-stu-id="c4e8b-106">The [Msimsp.exe](msimsp-exe.md) utility cannot be used to generate a patch package that applies a major upgrade.</span></span> <span data-ttu-id="c4e8b-107">En su lugar, aplique las actualizaciones principales, tal y como se describe en [aplicar actualizaciones principales instalando el producto](applying-major-upgrades-by-installing-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="c4e8b-107">Instead, apply major upgrades as described in [Applying Major Upgrades by Installing the Product](applying-major-upgrades-by-installing-the-product.md).</span></span>

 

<span data-ttu-id="c4e8b-108">**Para aplicar una revisión de actualización principal a una instalación local del producto**</span><span class="sxs-lookup"><span data-stu-id="c4e8b-108">**To apply a major upgrade patch to a local installation of the product**</span></span>

1.  <span data-ttu-id="c4e8b-109">Inicie la instalación de la revisión desde la línea de comandos o mediante un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="c4e8b-109">Launch the installation of the patch from the command line or by using an executable.</span></span> <span data-ttu-id="c4e8b-110">Para iniciar desde la línea de comandos, use msiexec/p patch. msp.</span><span class="sxs-lookup"><span data-stu-id="c4e8b-110">To launch from the command line, use msiexec /p patch.msp.</span></span> <span data-ttu-id="c4e8b-111">Para iniciar desde un archivo ejecutable, llame a [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) o al [**método ApplyPatch**](installer-applypatch.md) y proporcione los mismos argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="c4e8b-111">To launch from an executable, call [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) or the [**ApplyPatch Method**](installer-applypatch.md) and provide the same command line arguments.</span></span>
2.  <span data-ttu-id="c4e8b-112">Al aplicar una revisión a una instalación de cliente, el instalador omite el origen de instalación y continúa con la revisión de los archivos que ya están instalados en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="c4e8b-112">When patching a client installation, the installer ignores the installation source and proceeds to patch the files that are already installed on the user's computer.</span></span>
3.  <span data-ttu-id="c4e8b-113">El instalador cambia cualquier componente revisado marcado como ejecutar desde el origen a ejecución local.</span><span class="sxs-lookup"><span data-stu-id="c4e8b-113">The installer changes any patched components marked as run-from-source to run-locally.</span></span> <span data-ttu-id="c4e8b-114">Los usuarios no pueden ejecutar estos componentes desde el origen, siempre y cuando la revisión permanezca en el equipo.</span><span class="sxs-lookup"><span data-stu-id="c4e8b-114">Users are unable to run these components from the source as long as the patch remains on the computer.</span></span>
4.  <span data-ttu-id="c4e8b-115">El instalador agrega las transformaciones que se usan para actualizar el archivo. msi o agrega información específica de la revisión al perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="c4e8b-115">The installer adds any transforms used to update the .msi file or adds patch-specific information to the user's profile.</span></span>
5.  <span data-ttu-id="c4e8b-116">El instalador almacena en caché el archivo. msi en el equipo del usuario para que pueda realizar la instalación a petición, reinstalar y reparar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4e8b-116">The installer caches the .msi file on the user's computer so that it can perform installation-on-demand, reinstall, and repair of the application.</span></span> <span data-ttu-id="c4e8b-117">Después de aplicar una revisión a una instalación independiente, el instalador hace referencia a dos o más listas de origen a archivos externos: una para el origen original y otra para cada revisión que se ha aplicado.</span><span class="sxs-lookup"><span data-stu-id="c4e8b-117">After a patch is applied to a stand alone installation, the installer references two or more source lists to external files: one for the original source and one for each patch that has been applied.</span></span>

 

 



