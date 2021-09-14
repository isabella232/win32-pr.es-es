---
description: Este atributo especifica si los archivos de copia de seguridad de reversión se incluyen o no en los costos mostrados por el control VolumeCostList.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: ControlShowRollbackCost (atributo de control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7947777a356933ab74051163b6b9b023736dbb2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158762"
---
# <a name="controlshowrollbackcost-control-attribute"></a>ControlShowRollbackCost (atributo de control)

Este atributo especifica si los archivos de copia de seguridad de reversión se incluyen o no en los costos mostrados por el [control VolumeCostList](volumecostlist-control.md).

Si se establece este bit y la propiedad [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, los archivos de copia de seguridad de reversión se incluyen en el costo mostrado por el [control VolumeCostList](volumecostlist-control.md).

Si no se establece este bit y la propiedad [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, los archivos de copia de seguridad de reversión no se incluyen en el costo mostrado por el [control VolumeCostList](volumecostlist-control.md).

## <a name="valid-controls"></a>Controles válidos

[VolumeCostList](volumecostlist-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 4 194 304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

## <a name="remarks"></a>Observaciones

Este atributo de control se omite si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D o F.

Si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, se incluye el costo de la reversión, los archivos de copia de seguridad.

Si [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D o la propiedad [**DISABLEROLLBACK**](-disablerollback.md) = 1, no se incluye el costo de la reversión, los archivos de copia de seguridad.

 

 



