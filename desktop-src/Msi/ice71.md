---
description: ICE71 comprueba que la tabla de medios contiene una entrada con el valor de dipatine igual a 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002696"
---
# <a name="ice71"></a><span data-ttu-id="3debb-103">ICE71</span><span class="sxs-lookup"><span data-stu-id="3debb-103">ICE71</span></span>

<span data-ttu-id="3debb-104">ICE71 comprueba que la [tabla de medios](media-table.md) contiene una entrada con el valor de dipatine igual a 1.</span><span class="sxs-lookup"><span data-stu-id="3debb-104">ICE71 verifies that the [Media table](media-table.md) contains an entry with DiskId equal to 1.</span></span> <span data-ttu-id="3debb-105">(Windows Installer supone que el paquete. msi se encuentra en el disco 1).</span><span class="sxs-lookup"><span data-stu-id="3debb-105">(Windows Installer assumes that the .msi package is on disk 1.)</span></span>

## <a name="result"></a><span data-ttu-id="3debb-106">Resultado</span><span class="sxs-lookup"><span data-stu-id="3debb-106">Result</span></span>

<span data-ttu-id="3debb-107">ICE71 devuelve un error si la tabla de medios no contiene una entrada con el valor de dipatine igual a 1.</span><span class="sxs-lookup"><span data-stu-id="3debb-107">ICE71 returns an error if the Media table does not contain an entry with DiskId equal to 1.</span></span>

## <a name="example"></a><span data-ttu-id="3debb-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3debb-108">Example</span></span>

<span data-ttu-id="3debb-109">ICE71 notifica el siguiente error para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="3debb-109">ICE71 reports the following error for the example shown.</span></span>

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

<span data-ttu-id="3debb-110">T0 corrija este error, cambie el valor de la entrada en la que se almacena el paquete a 1.</span><span class="sxs-lookup"><span data-stu-id="3debb-110">T0 fix this error, change the DiskId of the entry where the package is stored to 1.</span></span>

<span data-ttu-id="3debb-111">[Tabla de medios](media-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="3debb-111">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="3debb-112">Detectaron</span><span class="sxs-lookup"><span data-stu-id="3debb-112">DiskId</span></span> |
|--------|
| <span data-ttu-id="3debb-113">2</span><span class="sxs-lookup"><span data-stu-id="3debb-113">2</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="3debb-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3debb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3debb-115">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="3debb-115">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



