---
description: Puede instalar ensamblados en paralelo como ensamblados compartidos o como ensamblados privados. Para obtener más información, vea Instalar ensamblados en paralelo como ensamblados privados e instalar ensamblados en paralelo como ensamblados compartidos.
ms.assetid: 36f271ff-be0c-4162-8e1c-86088ebddbcc
title: Instalar ensamblados en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be68580c7f0e3890c2e53b148daec92fbad18ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497231"
---
# <a name="installing-side-by-side-assemblies"></a><span data-ttu-id="3436a-104">Instalar ensamblados en paralelo</span><span class="sxs-lookup"><span data-stu-id="3436a-104">Installing Side-by-side Assemblies</span></span>

<span data-ttu-id="3436a-105">Puede instalar ensamblados en paralelo como [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies) o como [ensamblados privados](/windows/desktop/Msi/private-assemblies).</span><span class="sxs-lookup"><span data-stu-id="3436a-105">You may install side-by-side assemblies as [shared assemblies](/windows/desktop/Msi/shared-assemblies) or as [private assemblies](/windows/desktop/Msi/private-assemblies).</span></span> <span data-ttu-id="3436a-106">Para obtener más información, vea [Instalar ensamblados en paralelo como ensamblados privados](installing-side-by-side-assemblies-as-private-assemblies.md) e [Instalar ensamblados en paralelo como ensamblados compartidos](installing-side-by-side-assemblies-as-shared-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="3436a-106">For more information, see [Installing Side-by-Side Assemblies as Private Assemblies](installing-side-by-side-assemblies-as-private-assemblies.md) and [Installing Side-by-side Assemblies as Shared Assemblies](installing-side-by-side-assemblies-as-shared-assemblies.md).</span></span>

<span data-ttu-id="3436a-107">Observe lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3436a-107">Note that:</span></span>

-   <span data-ttu-id="3436a-108">Los ensamblados instalados en la caché global de ensamblados mediante una instalación de mediante el [contexto de instalación](/windows/desktop/Msi/installation-context) por usuario no están protegidos por protección de archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="3436a-108">Assemblies installed to the global assembly cache by an installation using the per-user [installation context](/windows/desktop/Msi/installation-context) are not protected by Windows File Protection.</span></span>
-   <span data-ttu-id="3436a-109">Los ensamblados que se instalan en la caché global de ensamblados mediante una instalación de mediante el [contexto de instalación](/windows/desktop/Msi/installation-context) por equipo están protegidos por protección de archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="3436a-109">Assemblies that are installed to the global assembly cache by an installation using the per-machine [installation context](/windows/desktop/Msi/installation-context) are protected by Windows File Protection.</span></span>

 

 
