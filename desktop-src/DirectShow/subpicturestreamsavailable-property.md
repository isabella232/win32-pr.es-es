---
description: La propiedad SubpictureStreamsAvailable recupera el número de secuencias de subimagen disponibles en el título actual.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Propiedad SubpictureStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e34f780a726966580a72d87b6f7900bb73c1a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688488"
---
# <a name="subpicturestreamsavailable-property"></a><span data-ttu-id="78666-103">Propiedad SubpictureStreamsAvailable</span><span class="sxs-lookup"><span data-stu-id="78666-103">SubpictureStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="78666-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="78666-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="78666-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="78666-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="78666-106">La `SubpictureStreamsAvailable` propiedad recupera el número de secuencias de subimagen disponibles en el título actual.</span><span class="sxs-lookup"><span data-stu-id="78666-106">The `SubpictureStreamsAvailable` property retrieves the number of subpicture streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="78666-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78666-107">Return Value</span></span>

<span data-ttu-id="78666-108">Devuelve el número de flujos disponibles como un entero.</span><span class="sxs-lookup"><span data-stu-id="78666-108">Returns the number of available streams as an Integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="78666-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78666-109">Remarks</span></span>

<span data-ttu-id="78666-110">Esta propiedad es de solo lectura y no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="78666-110">This property is read-only with no default value.</span></span> <span data-ttu-id="78666-111">Para consultar cada secuencia para su atributo Language, llame primero a este método para obtener el límite superior.</span><span class="sxs-lookup"><span data-stu-id="78666-111">To query each stream for its language attribute, first call this method to get the upper bound.</span></span>

<span data-ttu-id="78666-112">La numeración de secuencias es de base cero.</span><span class="sxs-lookup"><span data-stu-id="78666-112">Stream numbering is zero-based.</span></span>

 

 



