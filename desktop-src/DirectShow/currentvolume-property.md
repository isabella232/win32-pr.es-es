---
description: La propiedad CurrentVolume recupera el número de volumen del directorio raíz actual.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Propiedad CurrentVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677055"
---
# <a name="currentvolume-property"></a><span data-ttu-id="02403-103">Propiedad CurrentVolume</span><span class="sxs-lookup"><span data-stu-id="02403-103">CurrentVolume Property</span></span>

> [!Note]  
> <span data-ttu-id="02403-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="02403-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="02403-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="02403-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="02403-106">La `CurrentVolume` propiedad recupera el número de volumen del directorio raíz actual.</span><span class="sxs-lookup"><span data-stu-id="02403-106">The `CurrentVolume` property retrieves the volume number for the current root directory.</span></span>

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a><span data-ttu-id="02403-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02403-107">Return Value</span></span>

<span data-ttu-id="02403-108">Devuelve un valor entero que representa el volumen de DVD actual.</span><span class="sxs-lookup"><span data-stu-id="02403-108">Returns an integer value representing the current DVD volume.</span></span> <span data-ttu-id="02403-109">Si un disco forma parte de un conjunto de varios volúmenes, el valor entero debe ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="02403-109">If a disc is part of a multi-volume set, then the integer value should be greater than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="02403-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02403-110">Remarks</span></span>

<span data-ttu-id="02403-111">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="02403-111">This property is read-only with no default value.</span></span>

## <a name="see-also"></a><span data-ttu-id="02403-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="02403-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02403-113">**VolumesAvailable**</span><span class="sxs-lookup"><span data-stu-id="02403-113">**VolumesAvailable**</span></span>](volumesavailable-property.md)
</dt> </dl>

 

 



