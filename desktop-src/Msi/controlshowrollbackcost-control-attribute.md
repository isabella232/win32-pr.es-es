---
description: Este atributo especifica si los archivos de copia de seguridad de reversión se incluyen en los costos mostrados por el control VolumeCostList.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: Atributo de control ControlShowRollbackCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7947777a356933ab74051163b6b9b023736dbb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911914"
---
# <a name="controlshowrollbackcost-control-attribute"></a><span data-ttu-id="a8bf1-103">Atributo de control ControlShowRollbackCost</span><span class="sxs-lookup"><span data-stu-id="a8bf1-103">ControlShowRollbackCost Control Attribute</span></span>

<span data-ttu-id="a8bf1-104">Este atributo especifica si los archivos de copia de seguridad de reversión se incluyen en los costos mostrados por el [control VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="a8bf1-104">This attribute specifies whether or not the rollback backup files are included in the costs displayed by the [VolumeCostList control](volumecostlist-control.md).</span></span>

<span data-ttu-id="a8bf1-105">Si se establece este bit y [**PROMPTROLLBACKCOST**](promptrollbackcost.md) Property = P, los archivos de copia de seguridad de reversión se incluyen en el costo que muestra el [control VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="a8bf1-105">If this bit is set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

<span data-ttu-id="a8bf1-106">Si no se establece este bit y [**PROMPTROLLBACKCOST**](promptrollbackcost.md) Property = P, los archivos de copia de seguridad no se incluyen en el costo que muestra el [control VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="a8bf1-106">If this bit is not set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are not included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="a8bf1-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="a8bf1-107">Valid Controls</span></span>

[<span data-ttu-id="a8bf1-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="a8bf1-108">VolumeCostList</span></span>](volumecostlist-control.md)

## <a name="value"></a><span data-ttu-id="a8bf1-109">Value</span><span class="sxs-lookup"><span data-stu-id="a8bf1-109">Value</span></span>



| <span data-ttu-id="a8bf1-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="a8bf1-110">Decimal</span></span> | <span data-ttu-id="a8bf1-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="a8bf1-111">Hexadecimal</span></span> | <span data-ttu-id="a8bf1-112">Constante</span><span class="sxs-lookup"><span data-stu-id="a8bf1-112">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="a8bf1-113">4 194 304</span><span class="sxs-lookup"><span data-stu-id="a8bf1-113">4194304</span></span> | <span data-ttu-id="a8bf1-114">0x00400000</span><span class="sxs-lookup"><span data-stu-id="a8bf1-114">0x00400000</span></span>  | <span data-ttu-id="a8bf1-115">**msidbControlShowRollbackCost**</span><span class="sxs-lookup"><span data-stu-id="a8bf1-115">**msidbControlShowRollbackCost**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a8bf1-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8bf1-116">Remarks</span></span>

<span data-ttu-id="a8bf1-117">Este atributo de control se omite si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D o F.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-117">This control attribute is ignored if [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D or F.</span></span>

<span data-ttu-id="a8bf1-118">Si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, se incluye el costo de los archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-118">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, the cost of the rollback, backup files is included.</span></span>

<span data-ttu-id="a8bf1-119">Si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D, o la propiedad [**DISABLEROLLBACK**](-disablerollback.md) = 1, el costo de la reversión, no se incluyen los archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a8bf1-119">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D, or [**DISABLEROLLBACK**](-disablerollback.md) property = 1, the cost of the rollback, backup files is not included.</span></span>

 

 



