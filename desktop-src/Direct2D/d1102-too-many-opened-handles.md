---
title: D1102 demasiados identificadores abiertos
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Se encontró un gran número de interfaces no liberadas. Actualmente hay interfaces no liberadas asignadas por este archivo DLL.
keywords:
- D1102 demasiados identificadores abiertos Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e3c12c2e2a7b47535e830c6ed65a828a16672bbf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783587"
---
# <a name="d1102-too-many-opened-handles"></a><span data-ttu-id="08444-105">D1102: demasiados identificadores abiertos</span><span class="sxs-lookup"><span data-stu-id="08444-105">D1102: Too Many Opened Handles</span></span>

<span data-ttu-id="08444-106">Se encontró un gran número de interfaces no liberadas.</span><span class="sxs-lookup"><span data-stu-id="08444-106">A large number of unreleased interfaces were found.</span></span> <span data-ttu-id="08444-107">Actualmente \[  \] , el número de interfaces no liberadas asignadas por este archivo dll.</span><span class="sxs-lookup"><span data-stu-id="08444-107">Currently there are \[*number*\] unreleased interfaces allocated by this DLL.</span></span>

## <a name="placeholders"></a><span data-ttu-id="08444-108">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="08444-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="08444-109"><span id="number"></span><span id="NUMBER"></span>*números*</span><span class="sxs-lookup"><span data-stu-id="08444-109"><span id="number"></span><span id="NUMBER"></span>*number*</span></span>
</dt> <dd>

<span data-ttu-id="08444-110">Número de interfaces no liberadas asignadas por este archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="08444-110">The number of unreleased interfaces allocated by this DLL.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="08444-111">Nivel de error</span><span class="sxs-lookup"><span data-stu-id="08444-111">Error Level</span></span> | <span data-ttu-id="08444-112">Advertencia</span><span class="sxs-lookup"><span data-stu-id="08444-112">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="08444-113">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="08444-113">Possible Causes</span></span>

<span data-ttu-id="08444-114">Se creó un gran número de recursos.</span><span class="sxs-lookup"><span data-stu-id="08444-114">A large number of resources were created.</span></span> <span data-ttu-id="08444-115">Aunque Direct2D no tiene ningún límite superior en el número de recursos disponibles (excepto en la memoria), la capa de depuración emite este mensaje informativo cuando encuentra 1001 objetos activos, 2001 objetos activos o 3001 objetos activos, ya que esto podría indicar una fuga en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="08444-115">Although Direct2D has no upper bound on the number of available resources (except memory), the debug layer issues this informational message when it encounters 1001 live objects, 2001 live objects, or 3001 live objects etc, because this might indicate a leak in the application.</span></span>

 

 




