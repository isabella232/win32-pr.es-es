---
description: Componentes de BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Componentes de BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277980"
---
# <a name="blob-components"></a><span data-ttu-id="e3488-103">Componentes de BLOB</span><span class="sxs-lookup"><span data-stu-id="e3488-103">BLOB Components</span></span>

<span data-ttu-id="e3488-104">Un objeto binario grande (BLOB) incluye los siguientes componentes jerárquicos:</span><span class="sxs-lookup"><span data-stu-id="e3488-104">A binary large object (BLOB) includes the following hierarchical components:</span></span>

-   <span data-ttu-id="e3488-105">Propietarios</span><span class="sxs-lookup"><span data-stu-id="e3488-105">Owners</span></span>
-   <span data-ttu-id="e3488-106">Categorías</span><span class="sxs-lookup"><span data-stu-id="e3488-106">Categories</span></span>
-   <span data-ttu-id="e3488-107">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="e3488-107">Tags</span></span>
-   <span data-ttu-id="e3488-108">Valores</span><span class="sxs-lookup"><span data-stu-id="e3488-108">Values</span></span>

## <a name="textual-representation"></a><span data-ttu-id="e3488-109">Representación textual</span><span class="sxs-lookup"><span data-stu-id="e3488-109">Textual Representation</span></span>

<span data-ttu-id="e3488-110">Para mayor comodidad, los blobs aparecen en el formato propietario: Categoría: etiqueta: valor en el que aparecen cuando se guardan en un archivo.</span><span class="sxs-lookup"><span data-stu-id="e3488-110">For convenience, BLOBs appear in the Owner:Category:Tag:Value format that they appear in when saved to a file.</span></span> <span data-ttu-id="e3488-111">La estructura interna del BLOB es opaca porque representa punteros y tablas.</span><span class="sxs-lookup"><span data-stu-id="e3488-111">The internal structure of the BLOB is opaque because it represents pointers and tables.</span></span> <span data-ttu-id="e3488-112">Por ejemplo, esta es una entrada de un BLOB que se puede usar para configurar un NPP:</span><span class="sxs-lookup"><span data-stu-id="e3488-112">For example, here is an entry from a BLOB that can be used to configure an NPP:</span></span>

``` syntax
NPP:Configure:BufferSize=32768
```

<span data-ttu-id="e3488-113">El propietario es NPP.</span><span class="sxs-lookup"><span data-stu-id="e3488-113">The Owner is NPP.</span></span> <span data-ttu-id="e3488-114">La categoría es configure, la etiqueta es BufferSize y el valor es 32768.</span><span class="sxs-lookup"><span data-stu-id="e3488-114">The Category is Configure, the Tag is BufferSize, and the Value is 32768.</span></span>

 

 



