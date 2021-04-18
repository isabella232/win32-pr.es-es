---
description: En este ejemplo se muestra cómo localizar el paquete Windows Installer descrito en un ejemplo de instalación. El paquete de instalación original se ha cambiado de una versión en inglés al idioma francés.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Un ejemplo de localización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5ae0b04e65383d665e2532d45f0cc2eed856a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667074"
---
# <a name="a-localization-example"></a><span data-ttu-id="03ff1-104">Un ejemplo de localización</span><span class="sxs-lookup"><span data-stu-id="03ff1-104">A Localization Example</span></span>

<span data-ttu-id="03ff1-105">En este ejemplo se muestra cómo localizar el paquete Windows Installer descrito en [un ejemplo de instalación](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="03ff1-105">This example illustrates how to localize the Windows Installer package described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="03ff1-106">El paquete de instalación original se ha cambiado de una versión en inglés al idioma francés.</span><span class="sxs-lookup"><span data-stu-id="03ff1-106">The original installation package is changed from an English into French language version.</span></span>

<span data-ttu-id="03ff1-107">El ejemplo de localización tiene las siguientes especificaciones:</span><span class="sxs-lookup"><span data-stu-id="03ff1-107">The localization sample has the following specifications:</span></span>

-   <span data-ttu-id="03ff1-108">La interfaz de usuario de instalación de la aplicación MNP2000 debe cambiarse de inglés a francés.</span><span class="sxs-lookup"><span data-stu-id="03ff1-108">The installation UI for the application MNP2000 should be changed from English to French.</span></span>
-   <span data-ttu-id="03ff1-109">La versión en francés de MNP2000 incluye Readme.txt y Help.txt archivos escritos en el idioma francés.</span><span class="sxs-lookup"><span data-stu-id="03ff1-109">The French version of MNP2000 includes Readme.txt and Help.txt files written in the French language.</span></span>
-   <span data-ttu-id="03ff1-110">La versión en francés incluye una lista de los agentes de viaje en Francia que pueden proporcionar vales al terreno de estacionamiento rojo.</span><span class="sxs-lookup"><span data-stu-id="03ff1-110">The French version includes a list of travel agents in France that can provide tickets to Red Park Arena.</span></span> <span data-ttu-id="03ff1-111">Esta lista (proporcionada como un nuevo archivo, Fre.txt) no forma parte de la versión en inglés.</span><span class="sxs-lookup"><span data-stu-id="03ff1-111">This list (provided as a new file, Fre.txt) is not a part of the English version.</span></span>

<span data-ttu-id="03ff1-112">El procedimiento general para localizar una instalación de se describe en la sección [localizar un paquete de Windows Installer](localizing-a-windows-installer-package.md).</span><span class="sxs-lookup"><span data-stu-id="03ff1-112">The general procedure for localizing an installation is described in the section [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="03ff1-113">Copie la versión en Inglés de MNP2000.msi y todos los archivos de código fuente descritos en [planificación de la instalación](planning-the-installation.md) en una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="03ff1-113">Copy the English version of MNP2000.msi and all the source files described in [Planning the Installation](planning-the-installation.md) into a new folder.</span></span> <span data-ttu-id="03ff1-114">Cambie el nombre del MNP2000.msi en la carpeta a MNPFren.msi.</span><span class="sxs-lookup"><span data-stu-id="03ff1-114">Change the name of the MNP2000.msi in the folder to MNPFren.msi.</span></span> <span data-ttu-id="03ff1-115">En las secciones siguientes, modificará esta copia para localizar la aplicación en francés.</span><span class="sxs-lookup"><span data-stu-id="03ff1-115">In the following sections you will modify this copy to localize the application into French.</span></span>

[<span data-ttu-id="03ff1-116">Continuar</span><span class="sxs-lookup"><span data-stu-id="03ff1-116">Continue</span></span>](checking-the-installation-database-code-page.md)

 

 



