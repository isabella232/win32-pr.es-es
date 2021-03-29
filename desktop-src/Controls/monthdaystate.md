---
title: MONTHDAYSTATE
description: El tipo de datos MONTHDAYSTATE es un campo de bits que contiene el estado de cada día de un mes.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2286482460ec87982c46a564e8441edd9bf7bb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903151"
---
# <a name="monthdaystate"></a>MONTHDAYSTATE

El tipo de datos MONTHDAYSTATE es un campo de bits que contiene el estado de cada día de un mes. El tipo de datos se define en commctrl. h como se indica a continuación:


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



Cada bit (de 0 a 30) representa el estado de un día de un mes. Si un bit está activado, el día correspondiente se mostrará en negrita; en caso contrario, se mostrará sin énfasis.

Este tipo de datos se usa con el mensaje de [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) y la macro correspondiente, [**MonthCal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Cuando los valores de MONTHDAYSTATE se usan en referencia a meses más cortos que 31 días, solo se tendrá acceso a los bits necesarios.

Este tipo de datos se definió por primera vez en la [versión 4,70](common-control-versions.md) de Comctl32.dll.

 

 




