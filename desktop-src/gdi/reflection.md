---
description: Algunas aplicaciones proporcionan características que reflejan (o reflejar) objetos dibujados en el área de cliente.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Reflexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984838"
---
# <a name="reflection"></a><span data-ttu-id="7e784-103">Reflexión</span><span class="sxs-lookup"><span data-stu-id="7e784-103">Reflection</span></span>

<span data-ttu-id="7e784-104">Algunas aplicaciones proporcionan características que reflejan (o reflejar) objetos dibujados en el área de cliente.</span><span class="sxs-lookup"><span data-stu-id="7e784-104">Some applications provide features that reflect (or mirror) objects drawn in the client area.</span></span> <span data-ttu-id="7e784-105">Las aplicaciones que contienen capacidades de reflexión usan la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para establecer los valores adecuados en la transformación espacio global en el espacio de página.</span><span class="sxs-lookup"><span data-stu-id="7e784-105">Applications that contain reflection capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="7e784-106">Esta función recibe un puntero a una estructura [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) que contiene los valores adecuados.</span><span class="sxs-lookup"><span data-stu-id="7e784-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="7e784-107">Los miembros eM11 y eM22 de XFORM especifican los componentes de reflexión horizontal y vertical, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7e784-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical reflection components, respectively.</span></span>

<span data-ttu-id="7e784-108">La *transformación reflexión* crea una imagen reflejada de un objeto con respecto al eje x o y.</span><span class="sxs-lookup"><span data-stu-id="7e784-108">The *reflection transformation* creates a mirror image of an object with respect to either the x- or y-axis.</span></span> <span data-ttu-id="7e784-109">En Resumen, la reflexión es simplemente una escala negativa.</span><span class="sxs-lookup"><span data-stu-id="7e784-109">In short, reflection is just negative scaling.</span></span> <span data-ttu-id="7e784-110">Para generar una reflexión horizontal, las coordenadas x se multiplican por 1.</span><span class="sxs-lookup"><span data-stu-id="7e784-110">To produce a horizontal reflection, x-coordinates are multiplied by 1.</span></span> <span data-ttu-id="7e784-111">Para generar una reflexión vertical, las coordenadas y se multiplican por 1.</span><span class="sxs-lookup"><span data-stu-id="7e784-111">To produce a vertical reflection, y-coordinates are multiplied by 1.</span></span>

<span data-ttu-id="7e784-112">La reflexión horizontal se puede representar mediante el siguiente algoritmo:</span><span class="sxs-lookup"><span data-stu-id="7e784-112">Horizontal reflection can be represented by the following algorithm:</span></span>

``` syntax
x' = -x 
```

<span data-ttu-id="7e784-113">donde x es la coordenada x y x ' es el resultado de la reflexión.</span><span class="sxs-lookup"><span data-stu-id="7e784-113">where x is the x-coordinate and x' is the result of the reflection.</span></span>

<span data-ttu-id="7e784-114">La matriz de 2 por 2 que generó la reflexión horizontal contiene los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="7e784-114">The 2-by-2 matrix that produced horizontal reflection contains the following values:</span></span>

``` syntax
|-1    0| 
|0     1| 
```

<span data-ttu-id="7e784-115">La reflexión vertical se puede representar mediante el siguiente algoritmo:</span><span class="sxs-lookup"><span data-stu-id="7e784-115">Vertical reflection can be represented by the following algorithm:</span></span>

``` syntax
y' = -y 
```

<span data-ttu-id="7e784-116">donde y es la coordenada y y ' y ' es el resultado de la reflexión.</span><span class="sxs-lookup"><span data-stu-id="7e784-116">where y is the y-coordinate and y' is the result of the reflection.</span></span>

<span data-ttu-id="7e784-117">La matriz de 2 por 2 que generó la reflexión vertical contiene los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="7e784-117">The 2-by-2 matrix that produced vertical reflection contains the following values:</span></span>

``` syntax
|1    0| 
|0   -1| 
```

<span data-ttu-id="7e784-118">Las operaciones de reflexión horizontal y reflexión vertical se pueden combinar en una sola operación mediante la siguiente matriz de 2 por 2:</span><span class="sxs-lookup"><span data-stu-id="7e784-118">The horizontal-reflection and vertical-reflection operations can be combined into a single operation by using the following 2-by-2 matrix:</span></span>

``` syntax
|-1    0| 
|0    -1| 
```

 

 



