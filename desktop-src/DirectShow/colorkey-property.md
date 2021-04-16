---
description: La propiedad ColorKey establece o recupera la clave de color utilizada en los subtítulos (CC).
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Propiedad ColorKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494638"
---
# <a name="colorkey-property"></a><span data-ttu-id="5cf79-103">Propiedad ColorKey</span><span class="sxs-lookup"><span data-stu-id="5cf79-103">ColorKey Property</span></span>

> [!Note]  
> <span data-ttu-id="5cf79-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5cf79-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5cf79-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="5cf79-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5cf79-106">La `ColorKey` propiedad establece o recupera la clave de color utilizada en los subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="5cf79-106">The `ColorKey` property sets or retrieves the color key used in closed captioning.</span></span>

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a><span data-ttu-id="5cf79-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5cf79-107">Return Value</span></span>

<span data-ttu-id="5cf79-108">Devuelve un valor entero que representa el color que se va a usar como fondo transparente para el texto con título cerrado.</span><span class="sxs-lookup"><span data-stu-id="5cf79-108">Returns an integer value representing the color to use as a transparent background for closed-captioned text.</span></span> <span data-ttu-id="5cf79-109">El valor predeterminado en 256 colores es magenta y está fuera de negro en cualquier otra profundidad de color.</span><span class="sxs-lookup"><span data-stu-id="5cf79-109">The default value in 256 colors is magenta, and off-black in any other color depth.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cf79-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cf79-110">Remarks</span></span>

<span data-ttu-id="5cf79-111">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5cf79-111">This property is read/write.</span></span> <span data-ttu-id="5cf79-112">Esta propiedad solo se aplica a los subtítulos (CC), si existen, no a la secuencia de la subimagen.</span><span class="sxs-lookup"><span data-stu-id="5cf79-112">This property applies only to the closed-captions, if any exist, not to the subpicture stream.</span></span>

 

 



