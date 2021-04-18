---
title: Tipos de recursos
description: En este tema se describen los tipos de recursos de Direct3D 10, así como los nuevos tipos en Direct3D 11, incluidos los búferes estructurados y las texturas y los búferes de escritura.
ms.assetid: 9329f260-e806-4d6d-b6d1-3d001fad411a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3df57c5a4f6010df0494b6533a200d70be892e4
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420200"
---
# <a name="types-of-resources"></a><span data-ttu-id="48dc8-103">Tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="48dc8-103">Types of Resources</span></span>

<span data-ttu-id="48dc8-104">Los recursos son áreas de memoria a las que se puede tener acceso a través de la canalización de Direct3D, son los bloques de creación de la escena.</span><span class="sxs-lookup"><span data-stu-id="48dc8-104">Resources are areas in memory that can be accessed by the Direct3D pipeline, they are the building blocks of your scene.</span></span> <span data-ttu-id="48dc8-105">Los recursos contienen muchos tipos de datos, como geometría, texturas o datos de sombreador que Direct3D usa para rellenar y representar la escena.</span><span class="sxs-lookup"><span data-stu-id="48dc8-105">Resources contain many types of data such as geometry, textures or shader data that Direct3D uses to populate and render your scene.</span></span> <span data-ttu-id="48dc8-106">En este tema se describen los tipos de recursos de Direct3D 10, así como los nuevos tipos en Direct3D 11, incluidos los búferes estructurados y las texturas y los búferes de escritura.</span><span class="sxs-lookup"><span data-stu-id="48dc8-106">This topic describes the types of resources from Direct3D 10, as well as new types in Direct3D 11 including structured buffers and writable textures and buffers.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48dc8-107">Diferencias entre Direct3D 11 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="48dc8-107">Differences between Direct3D 11 and Direct3D 10:</span></span><br/> <span data-ttu-id="48dc8-108">Direct3D 11 admite varios tipos de recursos nuevos, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="48dc8-108">Direct3D 11 supports several new resource types including:</span></span><br/>
<ul>
<li><span data-ttu-id="48dc8-109"><a href="direct3d-11-advanced-stages-cs-resources.md">búferes y texturas de lectura y escritura</a></span><span class="sxs-lookup"><span data-stu-id="48dc8-109"><a href="direct3d-11-advanced-stages-cs-resources.md">read-write buffers and textures</a></span></span></li>
<li><span data-ttu-id="48dc8-110"><a href="direct3d-11-advanced-stages-cs-resources.md">búferes estructurados</a></span><span class="sxs-lookup"><span data-stu-id="48dc8-110"><a href="direct3d-11-advanced-stages-cs-resources.md">structured buffers</a></span></span></li>
<li><span data-ttu-id="48dc8-111"><a href="direct3d-11-advanced-stages-cs-resources.md">búferes de direcciones de bytes</a></span><span class="sxs-lookup"><span data-stu-id="48dc8-111"><a href="direct3d-11-advanced-stages-cs-resources.md">byte-address buffers</a></span></span></li>
<li><span data-ttu-id="48dc8-112"><a href="direct3d-11-advanced-stages-cs-resources.md">anexar y consumir búferes</a></span><span class="sxs-lookup"><span data-stu-id="48dc8-112"><a href="direct3d-11-advanced-stages-cs-resources.md">append and consume buffers</a></span></span></li>
<li><span data-ttu-id="48dc8-113"><a href="direct3d-11-advanced-stages-cs-resources.md">búfer o textura de acceso desordenado</a></span><span class="sxs-lookup"><span data-stu-id="48dc8-113"><a href="direct3d-11-advanced-stages-cs-resources.md">unordered access buffer or texture</a></span></span></li>
</ul>
<span data-ttu-id="48dc8-114">Direct3D 11,2 admite <a href="tiled-resources.md">recursos en mosaico</a>.</span><span class="sxs-lookup"><span data-stu-id="48dc8-114">Direct3D 11.2 supports <a href="tiled-resources.md">tiled resources</a>.</span></span><br/> <span data-ttu-id="48dc8-115">Tanto Direct3D 10 como Direct3D 11 admiten los tipos de <a href="overviews-direct3d-11-resources-textures-intro.md">textura</a> y <a href="overviews-direct3d-11-resources-buffers-intro.md">búfer</a> que se introdujeron en Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="48dc8-115">Both Direct3D 10 and Direct3D 11 support the <a href="overviews-direct3d-11-resources-buffers-intro.md">buffer</a> and <a href="overviews-direct3d-11-resources-textures-intro.md">texture</a> types that were introduced in Direct3D 10.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="48dc8-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="48dc8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48dc8-117">Recursos</span><span class="sxs-lookup"><span data-stu-id="48dc8-117">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





