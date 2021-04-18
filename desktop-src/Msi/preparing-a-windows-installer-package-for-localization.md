---
description: Siga estas instrucciones para facilitar la localización de Windows Installer paquetes.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Preparación de un paquete de Windows Installer para la localización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652363"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a><span data-ttu-id="e51ca-103">Preparación de un paquete de Windows Installer para la localización</span><span class="sxs-lookup"><span data-stu-id="e51ca-103">Preparing a Windows Installer Package for Localization</span></span>

<span data-ttu-id="e51ca-104">La localización de un paquete de Windows Installer en varios idiomas puede facilitarse enormemente haciendo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e51ca-104">Localization of a Windows Installer package into multiple languages can be greatly facilitated by doing the following:</span></span>

-   <span data-ttu-id="e51ca-105">Cree una base de datos de instalación básica que tenga una página de códigos neutra.</span><span class="sxs-lookup"><span data-stu-id="e51ca-105">Author a base installation database that is code page neutral.</span></span> <span data-ttu-id="e51ca-106">Vea [crear una base de datos con una página de códigos neutra](creating-a-database-with-a-neutral-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="e51ca-106">See [Creating a database with a neutral code page](creating-a-database-with-a-neutral-code-page.md).</span></span> <span data-ttu-id="e51ca-107">La página de códigos de la base de datos localizada se puede establecer importando una tabla de archivo de texto con una página de códigos no neutra en la base de datos base.</span><span class="sxs-lookup"><span data-stu-id="e51ca-107">The code page of the localized database can then be set by importing a text archive table with a non-neutral code page into the base database.</span></span> <span data-ttu-id="e51ca-108">Vea [establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="e51ca-108">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="e51ca-109">Organice los archivos que requieren localización en componentes independientes e instálelos en directorios independientes.</span><span class="sxs-lookup"><span data-stu-id="e51ca-109">Organize files requiring localization into separate components and install these files into separate directories.</span></span> <span data-ttu-id="e51ca-110">Esto garantiza que dos paquetes localizados nunca instalan archivos con el mismo nombre en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="e51ca-110">This ensures that two localized packages never install identically named files into the same directory.</span></span>

<span data-ttu-id="e51ca-111">Por ejemplo, una aplicación de todo el mundo que usa los siguientes recursos puede tener tres componentes.</span><span class="sxs-lookup"><span data-stu-id="e51ca-111">For example, a worldwide application using the following resources may have three components.</span></span>



| <span data-ttu-id="e51ca-112">Componente</span><span class="sxs-lookup"><span data-stu-id="e51ca-112">Component</span></span> | <span data-ttu-id="e51ca-113">Recurso</span><span class="sxs-lookup"><span data-stu-id="e51ca-113">Resource</span></span>                   |
|-----------|----------------------------|
| <span data-ttu-id="e51ca-114">WWPN</span><span class="sxs-lookup"><span data-stu-id="e51ca-114">WORLD</span></span>     | <span data-ttu-id="e51ca-115">worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="e51ca-115">worldwide.exe</span></span>              |
| <span data-ttu-id="e51ca-116">WWPN</span><span class="sxs-lookup"><span data-stu-id="e51ca-116">WORLD</span></span>     | <span data-ttu-id="e51ca-117">entradas del registro en todo el mundo</span><span class="sxs-lookup"><span data-stu-id="e51ca-117">worldwide registry entries</span></span> |
| <span data-ttu-id="e51ca-118">WWPN</span><span class="sxs-lookup"><span data-stu-id="e51ca-118">WORLD</span></span>     | <span data-ttu-id="e51ca-119">acceso directo internacional</span><span class="sxs-lookup"><span data-stu-id="e51ca-119">worldwide shortcut</span></span>         |
| <span data-ttu-id="e51ca-120">ESN</span><span class="sxs-lookup"><span data-stu-id="e51ca-120">ENG</span></span>       | <span data-ttu-id="e51ca-121">engui.dll</span><span class="sxs-lookup"><span data-stu-id="e51ca-121">engui.dll</span></span>                  |
| <span data-ttu-id="e51ca-122">ESN</span><span class="sxs-lookup"><span data-stu-id="e51ca-122">ENG</span></span>       | <span data-ttu-id="e51ca-123">readme.txt</span><span class="sxs-lookup"><span data-stu-id="e51ca-123">readme.txt</span></span>                 |
| <span data-ttu-id="e51ca-124">FRA</span><span class="sxs-lookup"><span data-stu-id="e51ca-124">FRA</span></span>       | <span data-ttu-id="e51ca-125">fraui.dll</span><span class="sxs-lookup"><span data-stu-id="e51ca-125">fraui.dll</span></span>                  |
| <span data-ttu-id="e51ca-126">FRA</span><span class="sxs-lookup"><span data-stu-id="e51ca-126">FRA</span></span>       | <span data-ttu-id="e51ca-127">readme.txt</span><span class="sxs-lookup"><span data-stu-id="e51ca-127">readme.txt</span></span>                 |



 

<span data-ttu-id="e51ca-128">Los archivos que deben localizarse se pueden instalar en las siguientes ubicaciones de directorio:</span><span class="sxs-lookup"><span data-stu-id="e51ca-128">The files that need to be localized may be installed into the following directory locations:</span></span>

-   <span data-ttu-id="e51ca-129">\[\] \\worldwide.exe del mundo de ProgramFilesFolder \\</span><span class="sxs-lookup"><span data-stu-id="e51ca-129">\[ProgramFilesFolder\]\\World\\worldwide.exe</span></span>
-   <span data-ttu-id="e51ca-130">\[ProgramFilesFolder \] \\ World \\ English \\engui.dll</span><span class="sxs-lookup"><span data-stu-id="e51ca-130">\[ProgramFilesFolder\]\\World\\English\\engui.dll</span></span>
-   <span data-ttu-id="e51ca-131">\[ProgramFilesFolder \] \\ World \\ English \\readme.txt</span><span class="sxs-lookup"><span data-stu-id="e51ca-131">\[ProgramFilesFolder\]\\World\\English\\readme.txt</span></span>
-   <span data-ttu-id="e51ca-132">\[\] \\fraui.dll en \\ francés del mundo \\ de ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="e51ca-132">\[ProgramFilesFolder\]\\World\\French\\fraui.dll</span></span>
-   <span data-ttu-id="e51ca-133">\[\] \\readme.txt en \\ francés del mundo \\ de ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="e51ca-133">\[ProgramFilesFolder\]\\World\\French\\readme.txt</span></span>

 

 



