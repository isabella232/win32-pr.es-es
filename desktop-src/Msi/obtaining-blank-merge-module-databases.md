---
description: Obtener una base de datos de módulo de mezcla en blanco. Puede usar el archivo Schema. MSM proporcionado con el SDK de Windows Installer como base de datos de inicio para el módulo de combinación. Para obtener más información, vea componentes de Windows SDK para desarrolladores de Windows Installer.
ms.assetid: 8408e892-adc6-4ef5-ad36-4d04c021c899
title: Obtener las bases de datos del módulo de combinación en blanco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba75d55763d30b0ab545d2dbddbc19c1b0c279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677625"
---
# <a name="obtaining-blank-merge-module-databases"></a><span data-ttu-id="cc79e-105">Obtener las bases de datos del módulo de combinación en blanco</span><span class="sxs-lookup"><span data-stu-id="cc79e-105">Obtaining Blank Merge Module Databases</span></span>

<span data-ttu-id="cc79e-106">Obtener una base de datos de módulo de mezcla en blanco.</span><span class="sxs-lookup"><span data-stu-id="cc79e-106">Obtain a blank merge module database.</span></span> <span data-ttu-id="cc79e-107">Puede usar el archivo Schema. MSM proporcionado con el SDK de Windows Installer como base de datos de inicio para el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="cc79e-107">You can use the file Schema.msm provided with the Windows Installer SDK as a starting database for your merge module.</span></span> <span data-ttu-id="cc79e-108">Para obtener más información, vea [componentes de Windows SDK para desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="cc79e-108">For more information, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="cc79e-109">Los desarrolladores deben crear módulos de combinación con el esquema de base de datos más simple que instala sus componentes.</span><span class="sxs-lookup"><span data-stu-id="cc79e-109">Developers should author merge modules using the simplest database schema that installs their components.</span></span> <span data-ttu-id="cc79e-110">El uso de un esquema simple garantiza la mayor compatibilidad para el módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="cc79e-110">The use of a simple schema ensures the greatest compatibility for the merge module.</span></span> <span data-ttu-id="cc79e-111">La combinación de un módulo de combinación en un paquete de instalación con un esquema de base de datos diferente normalmente produce conflictos de combinación.</span><span class="sxs-lookup"><span data-stu-id="cc79e-111">Merging a merge module into an installation package with a different database schema usually results in merge conflicts.</span></span>

<span data-ttu-id="cc79e-112">Para obtener una lista completa de todas las tablas necesarias y opcionales en los módulos de combinación, vea [Merge Module Database tables](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="cc79e-112">For a complete list of all the required and optional tables in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span>

 

 



