---
description: Puede usar el instalador para agregar la información de una base de datos a otra base de datos mediante una combinación.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Combinar bases de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002559"
---
# <a name="merging-databases"></a><span data-ttu-id="650dd-103">Combinar bases de datos</span><span class="sxs-lookup"><span data-stu-id="650dd-103">Merging Databases</span></span>

<span data-ttu-id="650dd-104">Puede usar el instalador para agregar la información de una base de datos a otra base de datos mediante una combinación.</span><span class="sxs-lookup"><span data-stu-id="650dd-104">You can use the installer to add the information in one database into another database by performing a merge.</span></span> <span data-ttu-id="650dd-105">Las [combinaciones y transformaciones](merges-and-transforms.md) operan en una base de datos completa y una combinación combina dos bases de datos en una.</span><span class="sxs-lookup"><span data-stu-id="650dd-105">[Merges and Transforms](merges-and-transforms.md) operate on an entire database, and a merge combines two databases into one.</span></span> <span data-ttu-id="650dd-106">Las combinaciones son útiles para los equipos de desarrollo porque permiten que la base de datos de instalación de aplicaciones de gran tamaño se divida en partes más pequeñas y, posteriormente, se vuelvan a combinar en la base de datos de instalación completa.</span><span class="sxs-lookup"><span data-stu-id="650dd-106">Merges are useful to development teams because they allow the installation database of large application to be divided into smaller parts and then recombined into the complete installation database later.</span></span>

<span data-ttu-id="650dd-107">**Para combinar varias bases de datos de componentes en una sola base de datos completa**</span><span class="sxs-lookup"><span data-stu-id="650dd-107">**To merge several component databases into a single complete database**</span></span>

1.  <span data-ttu-id="650dd-108">Desarrolle las bases de datos de componentes parciales por separado.</span><span class="sxs-lookup"><span data-stu-id="650dd-108">Develop the partial component databases separately.</span></span>
2.  <span data-ttu-id="650dd-109">Combine cada base de datos de componentes en la base de datos principal del producto llamando a la función [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) .</span><span class="sxs-lookup"><span data-stu-id="650dd-109">Merge each component database into the main product database by calling the [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) function.</span></span>

 

 



