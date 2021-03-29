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
# <a name="monthdaystate"></a><span data-ttu-id="75a03-103">MONTHDAYSTATE</span><span class="sxs-lookup"><span data-stu-id="75a03-103">MONTHDAYSTATE</span></span>

<span data-ttu-id="75a03-104">El tipo de datos MONTHDAYSTATE es un campo de bits que contiene el estado de cada día de un mes.</span><span class="sxs-lookup"><span data-stu-id="75a03-104">The MONTHDAYSTATE data type is a bitfield that holds the state of each day in a month.</span></span> <span data-ttu-id="75a03-105">El tipo de datos se define en commctrl. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="75a03-105">The data type is defined in Commctrl.h as follows:</span></span>


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



<span data-ttu-id="75a03-106">Cada bit (de 0 a 30) representa el estado de un día de un mes.</span><span class="sxs-lookup"><span data-stu-id="75a03-106">Each bit (0 through 30) represents the state of a day in a month.</span></span> <span data-ttu-id="75a03-107">Si un bit está activado, el día correspondiente se mostrará en negrita; en caso contrario, se mostrará sin énfasis.</span><span class="sxs-lookup"><span data-stu-id="75a03-107">If a bit is on, the corresponding day will be displayed in bold; otherwise it will be displayed with no emphasis.</span></span>

<span data-ttu-id="75a03-108">Este tipo de datos se usa con el mensaje de [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) y la macro correspondiente, [**MonthCal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span><span class="sxs-lookup"><span data-stu-id="75a03-108">This data type is used with the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message and the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="75a03-109">Cuando los valores de MONTHDAYSTATE se usan en referencia a meses más cortos que 31 días, solo se tendrá acceso a los bits necesarios.</span><span class="sxs-lookup"><span data-stu-id="75a03-109">When MONTHDAYSTATE values are used in reference to months shorter than 31 days, only the needed bits will be accessed.</span></span>

<span data-ttu-id="75a03-110">Este tipo de datos se definió por primera vez en la [versión 4,70](common-control-versions.md) de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="75a03-110">This data type was first defined in [Version 4.70](common-control-versions.md) of Comctl32.dll.</span></span>

 

 




