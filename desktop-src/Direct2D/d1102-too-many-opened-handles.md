---
title: D1102 Demasiados identificadores abiertos
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Se encontró un gran número de interfaces no publicados. Actualmente hay interfaces no disponibles asignadas por este archivo DLL.
keywords:
- D1102 Demasiados identificadores abiertos direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2d59e110aece56a31af71e75e9a8eca0bb008961
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548690"
---
# <a name="d1102-too-many-opened-handles"></a><span data-ttu-id="86ee1-105">D1102: Demasiados identificadores abiertos</span><span class="sxs-lookup"><span data-stu-id="86ee1-105">D1102: Too Many Opened Handles</span></span>

<span data-ttu-id="86ee1-106">Se encontró un gran número de interfaces no publicados.</span><span class="sxs-lookup"><span data-stu-id="86ee1-106">A large number of unreleased interfaces were found.</span></span> <span data-ttu-id="86ee1-107">Actualmente hay número \[ *de* \] interfaces no publicados asignadas por este archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="86ee1-107">Currently there are \[*number*\] unreleased interfaces allocated by this DLL.</span></span>

## <a name="placeholders"></a><span data-ttu-id="86ee1-108">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="86ee1-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="86ee1-109"><span id="number"></span><span id="NUMBER"></span>*Número*</span><span class="sxs-lookup"><span data-stu-id="86ee1-109"><span id="number"></span><span id="NUMBER"></span>*number*</span></span>
</dt> <dd>

<span data-ttu-id="86ee1-110">Número de interfaces no publicados asignadas por este archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="86ee1-110">The number of unreleased interfaces allocated by this DLL.</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="86ee1-111">Nivel de error</span><span class="sxs-lookup"><span data-stu-id="86ee1-111">Error Level</span></span> | <span data-ttu-id="86ee1-112">Advertencia</span><span class="sxs-lookup"><span data-stu-id="86ee1-112">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="86ee1-113">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="86ee1-113">Possible Causes</span></span>

<span data-ttu-id="86ee1-114">Se creó un gran número de recursos.</span><span class="sxs-lookup"><span data-stu-id="86ee1-114">A large number of resources were created.</span></span> <span data-ttu-id="86ee1-115">Aunque Direct2D no tiene ningún límite superior en el número de recursos disponibles (excepto memoria), la capa de depuración emite este mensaje informativo cuando encuentra 1001 objetos en directo, 2001 objetos en directo o 3001 objetos en directo, etc., porque esto podría indicar una pérdida en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="86ee1-115">Although Direct2D has no upper bound on the number of available resources (except memory), the debug layer issues this informational message when it encounters 1001 live objects, 2001 live objects, or 3001 live objects etc, because this might indicate a leak in the application.</span></span>

 

 




