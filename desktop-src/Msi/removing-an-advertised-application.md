---
description: Para quitar una aplicación que se ha instalado en el estado anunciado, simplemente desinstálelo mediante MsiInstallProduct o MsiConfigureProduct. También puede quitar una aplicación anunciada de la línea de comandos. Vea opciones de la línea de comandos.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Quitar una aplicación anunciada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910694"
---
# <a name="removing-an-advertised-application"></a><span data-ttu-id="5e6d9-105">Quitar una aplicación anunciada</span><span class="sxs-lookup"><span data-stu-id="5e6d9-105">Removing an Advertised Application</span></span>

<span data-ttu-id="5e6d9-106">Para quitar una aplicación que se ha instalado en el estado anunciado, simplemente desinstálelo mediante [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span><span class="sxs-lookup"><span data-stu-id="5e6d9-106">To remove an application that has been installed in the advertised state, simply uninstall it using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta).</span></span> <span data-ttu-id="5e6d9-107">También puede quitar una aplicación anunciada de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-107">You can also remove an advertised application from the command line.</span></span> <span data-ttu-id="5e6d9-108">Vea [Opciones](command-line-options.md)de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-108">See [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="5e6d9-109">Tenga en cuenta que es posible que no pueda quitar una aplicación anunciada si ha creado el paquete de forma que la ejecución de una instalación sea condicional en la instrucción **no instalada**.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-109">Note that you may be unable to remove an advertised application if you have authored the package in such a way that running an installation is conditional upon the statement **NOT Installed**.</span></span> <span data-ttu-id="5e6d9-110">Una aplicación anunciada no está instalada en el equipo del usuario y el instalador no establece la propiedad [**instalado**](installed.md) .</span><span class="sxs-lookup"><span data-stu-id="5e6d9-110">An advertised application is not installed on the user's computer and the installer does not set the [**Installed**](installed.md) Property.</span></span> <span data-ttu-id="5e6d9-111">Se debe crear el paquete para que se puedan desinstalar las aplicaciones anunciadas.</span><span class="sxs-lookup"><span data-stu-id="5e6d9-111">The package must be authored so that advertised applications can be uninstalled.</span></span>

 

 



