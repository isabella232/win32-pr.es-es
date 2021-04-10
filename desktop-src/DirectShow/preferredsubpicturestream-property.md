---
description: La propiedad PreferredSubpictureStream recupera la secuencia de subimagen preferida para la sesión de visualización actual.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Propiedad PreferredSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23377d74d3632c665b001ae415dc151ca73bd148
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906602"
---
# <a name="preferredsubpicturestream-property"></a><span data-ttu-id="b0295-103">Propiedad PreferredSubpictureStream</span><span class="sxs-lookup"><span data-stu-id="b0295-103">PreferredSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="b0295-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b0295-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b0295-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="b0295-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b0295-106">La `PreferredSubpictureStream` propiedad recupera la secuencia de subimagen preferida para la sesión de visualización actual.</span><span class="sxs-lookup"><span data-stu-id="b0295-106">The `PreferredSubpictureStream` property retrieves the preferred subpicture stream for the current viewing session.</span></span>

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="b0295-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0295-107">Return Value</span></span>

<span data-ttu-id="b0295-108">Devuelve un valor entero que representa la secuencia de la subimagen preferida actual en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="b0295-108">Returns an Integer value representing the current preferred subpicture stream in the system registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0295-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0295-109">Remarks</span></span>

<span data-ttu-id="b0295-110">La secuencia de subimagen preferida se establece con [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)del objeto [MSDVDAdm](msdvdadm-object.md) .</span><span class="sxs-lookup"><span data-stu-id="b0295-110">The preferred subpicture stream is set with [MSDVDAdm](msdvdadm-object.md) object's [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md).</span></span>

 

 



