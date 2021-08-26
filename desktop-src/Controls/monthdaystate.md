---
title: MONTHDAYSTATE
description: El tipo de datos MONTHDAYSTATE es un campo de bits que contiene el estado de cada día de un mes.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e21eed1293a53bce8f38f5bd4db09b8cbe3fbf649fb07348a5dca65e908727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079865"
---
# <a name="monthdaystate"></a>MONTHDAYSTATE

El tipo de datos MONTHDAYSTATE es un campo de bits que contiene el estado de cada día de un mes. El tipo de datos se define en Commctrl.h de la siguiente manera:


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



Cada bit (de 0 a 30) representa el estado de un día en un mes. Si un bit está en, el día correspondiente se mostrará en negrita; De lo contrario, se mostrará sin énfasis.

Este tipo de datos se usa con el [**mensaje \_ SETDAYSTATE**](mcm-setdaystate.md) de MCM y la macro correspondiente, [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Cuando se usan valores MONTHDAYSTATE en referencia a meses inferiores a 31 días, solo se accederá a los bits necesarios.

Este tipo de datos se definió por primera vez en [la versión 4.70](common-control-versions.md) de Comctl32.dll.

 

 




