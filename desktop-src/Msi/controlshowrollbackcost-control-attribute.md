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
# <a name="controlshowrollbackcost-control-attribute"></a>Atributo de control ControlShowRollbackCost

Este atributo especifica si los archivos de copia de seguridad de reversión se incluyen en los costos mostrados por el [control VolumeCostList](volumecostlist-control.md).

Si se establece este bit y [**PROMPTROLLBACKCOST**](promptrollbackcost.md) Property = P, los archivos de copia de seguridad de reversión se incluyen en el costo que muestra el [control VolumeCostList](volumecostlist-control.md).

Si no se establece este bit y [**PROMPTROLLBACKCOST**](promptrollbackcost.md) Property = P, los archivos de copia de seguridad no se incluyen en el costo que muestra el [control VolumeCostList](volumecostlist-control.md).

## <a name="valid-controls"></a>Controles válidos

[VolumeCostList](volumecostlist-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 4 194 304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

## <a name="remarks"></a>Observaciones

Este atributo de control se omite si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D o F.

Si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, se incluye el costo de los archivos de copia de seguridad.

Si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D, o la propiedad [**DISABLEROLLBACK**](-disablerollback.md) = 1, el costo de la reversión, no se incluyen los archivos de copia de seguridad.

 

 



