---
description: La propiedad VolumesAvailable recupera el número de volúmenes de un conjunto de varios volúmenes.
ms.assetid: d056b6d5-f4a4-480b-96a5-8e95dce23dfb
title: Propiedad VolumesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccdcf32ba8b7bea3958ef469bc0f90f9d41ecc14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687860"
---
# <a name="volumesavailable-property"></a><span data-ttu-id="7a102-103">Propiedad VolumesAvailable</span><span class="sxs-lookup"><span data-stu-id="7a102-103">VolumesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="7a102-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7a102-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7a102-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="7a102-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7a102-106">La `VolumesAvailable` propiedad recupera el número de volúmenes de un conjunto de varios volúmenes.</span><span class="sxs-lookup"><span data-stu-id="7a102-106">The `VolumesAvailable` property retrieves the number of volumes in a multivolume set.</span></span>

``` syntax
[ iVolumes = ] MSWebDVD.VolumesAvailable
```

## <a name="return-value"></a><span data-ttu-id="7a102-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a102-107">Return Value</span></span>

<span data-ttu-id="7a102-108">Devuelve el número de volúmenes del conjunto como un entero.</span><span class="sxs-lookup"><span data-stu-id="7a102-108">Returns the number of volumes in the set as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a102-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a102-109">Remarks</span></span>

<span data-ttu-id="7a102-110">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7a102-110">This property is read-only with no default value.</span></span> <span data-ttu-id="7a102-111">Algunos títulos de DVD se pueden publicar como una serie o conjunto de varios discos.</span><span class="sxs-lookup"><span data-stu-id="7a102-111">Some DVD titles might be released as a multidisc set or series.</span></span> <span data-ttu-id="7a102-112">Utilice este método para determinar el número de volumen del disco actual.</span><span class="sxs-lookup"><span data-stu-id="7a102-112">Use this method to determine the volume number for the current disc.</span></span>

 

 



