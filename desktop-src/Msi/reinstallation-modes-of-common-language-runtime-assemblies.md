---
description: Los ensamblados de Common Language Runtime que se instalan en la caché global de ensamblados deben tener archivos idénticos en todas las apariciones del ensamblado.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Modos de reinstalación de los ensamblados de Common Language Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667149"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a><span data-ttu-id="014ac-103">Modos de reinstalación de los ensamblados de Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="014ac-103">Reinstallation Modes of Common Language Runtime Assemblies</span></span>

<span data-ttu-id="014ac-104">Los ensamblados de Common Language Runtime que se instalan en la caché global de ensamblados deben tener archivos idénticos en todas las apariciones del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="014ac-104">Common language runtime assemblies that are installed to the global assembly cache must have identical files in all occurrences of the assembly.</span></span> <span data-ttu-id="014ac-105">Esto significa que los modos de reinstalación usados por [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) y [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) deben tener significados diferentes para los componentes normales y los ensamblados de Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="014ac-105">This means that the reinstallation modes used by [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) and [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) must have different meanings for regular components and common language runtime assemblies.</span></span> <span data-ttu-id="014ac-106">Las siguientes definiciones de modos de reinstalación se aplican a ensamblados de Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="014ac-106">The following definitions of reinstall modes apply to common language runtime assemblies.</span></span>



| <span data-ttu-id="014ac-107">Modo de reinstalación</span><span class="sxs-lookup"><span data-stu-id="014ac-107">Reinstall mode</span></span>                  | <span data-ttu-id="014ac-108">Significado de los componentes de Microsoft .NET</span><span class="sxs-lookup"><span data-stu-id="014ac-108">Meaning for Microsoft .NET Components</span></span>                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="014ac-109">REINSTALLMODE \_ FILEMISSING</span><span class="sxs-lookup"><span data-stu-id="014ac-109">REINSTALLMODE\_FILEMISSING</span></span>      | <span data-ttu-id="014ac-110">Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.</span><span class="sxs-lookup"><span data-stu-id="014ac-110">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="014ac-111">REINSTALLMODE \_ FILEOLDERVERSION</span><span class="sxs-lookup"><span data-stu-id="014ac-111">REINSTALLMODE\_FILEOLDERVERSION</span></span> | <span data-ttu-id="014ac-112">Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.</span><span class="sxs-lookup"><span data-stu-id="014ac-112">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="014ac-113">REINSTALLMODE \_ FILEEQUALVERSION</span><span class="sxs-lookup"><span data-stu-id="014ac-113">REINSTALLMODE\_FILEEQUALVERSION</span></span> | <span data-ttu-id="014ac-114">Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.</span><span class="sxs-lookup"><span data-stu-id="014ac-114">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="014ac-115">REINSTALLMODE \_ FILEEXACT</span><span class="sxs-lookup"><span data-stu-id="014ac-115">REINSTALLMODE\_FILEEXACT</span></span>        | <span data-ttu-id="014ac-116">Instale o vuelva a instalar el componente de Common Language Runtime si falta o está incompleto.</span><span class="sxs-lookup"><span data-stu-id="014ac-116">Install or reinstall the common language runtime component if it is missing or incomplete.</span></span>                                         |
| <span data-ttu-id="014ac-117">REINSTALLMODE \_ FILEVERIFY</span><span class="sxs-lookup"><span data-stu-id="014ac-117">REINSTALLMODE\_FILEVERIFY</span></span>       | <span data-ttu-id="014ac-118">Instale o vuelva a instalar el componente de Common Language Runtime si falta o si el componente existente está incompleto o dañado.</span><span class="sxs-lookup"><span data-stu-id="014ac-118">Install or reinstall the common language runtime component if it is missing or if the existing component is incomplete or corrupt.</span></span> |
| <span data-ttu-id="014ac-119">REINSTALLMODE \_ FILEREPLACE</span><span class="sxs-lookup"><span data-stu-id="014ac-119">REINSTALLMODE\_FILEREPLACE</span></span>      | <span data-ttu-id="014ac-120">Instale o vuelva a instalar siempre el componente Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="014ac-120">Always install or reinstall the common language runtime component.</span></span>                                                                 |



 

 

 



