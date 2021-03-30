---
description: Las transformaciones incrustadas se almacenan en el archivo. msi del paquete. Esto garantiza a los usuarios que la transformación está siempre disponible cuando el paquete de instalación está disponible. Como alternativa, se pueden proporcionar transformaciones a los usuarios como archivos. MST independientes.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Transformaciones incrustadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082780"
---
# <a name="embedded-transforms"></a><span data-ttu-id="57d72-105">Transformaciones incrustadas</span><span class="sxs-lookup"><span data-stu-id="57d72-105">Embedded Transforms</span></span>

<span data-ttu-id="57d72-106">Las transformaciones incrustadas se almacenan en el archivo. msi del paquete.</span><span class="sxs-lookup"><span data-stu-id="57d72-106">Embedded transforms are stored inside the .msi file of the package.</span></span> <span data-ttu-id="57d72-107">Esto garantiza a los usuarios que la transformación está siempre disponible cuando el paquete de instalación está disponible.</span><span class="sxs-lookup"><span data-stu-id="57d72-107">This guarantees to users that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="57d72-108">Como alternativa, se pueden proporcionar transformaciones a los usuarios como archivos. MST independientes.</span><span class="sxs-lookup"><span data-stu-id="57d72-108">Alternatively, transforms may be provided to users as standalone .mst files.</span></span>

<span data-ttu-id="57d72-109">Para agregar una transformación incrustada a la lista transformaciones, agregue un signo de dos puntos (:) prefijo al nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="57d72-109">To add an embedded transform to the transforms list, add a colon (:) prefix to the file name.</span></span> <span data-ttu-id="57d72-110">Dado que el instalador siempre puede obtener la transformación del almacenamiento en el archivo. msi, las transformaciones incrustadas no se almacenan en caché en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="57d72-110">Because the installer can always obtain the transform from storage in the .msi file, embedded transforms are not cached on the user's computer.</span></span> <span data-ttu-id="57d72-111">Las transformaciones incrustadas se pueden usar en combinación con transformaciones [protegidas](secured-transforms.md) o [transformaciones no seguras](unsecured-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="57d72-111">Embedded transforms may be used in combination with [secured transforms](secured-transforms.md) or [unsecured transforms](unsecured-transforms.md).</span></span> <span data-ttu-id="57d72-112">Para obtener más información, vea [aplicar transformaciones](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="57d72-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



