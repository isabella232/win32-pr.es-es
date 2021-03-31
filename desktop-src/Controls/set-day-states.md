---
title: Establecimiento de los Estados de día
description: En este tema se muestra cómo establecer la información de estado de día. El control de calendario mensual utiliza información de estado de día para determinar cómo dibuja determinados días dentro del control.
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa1fc105c94a15e1a658218013dca00129c883c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995771"
---
# <a name="how-to-set-day-states"></a><span data-ttu-id="136eb-104">Establecimiento de los Estados de día</span><span class="sxs-lookup"><span data-stu-id="136eb-104">How to Set Day States</span></span>

<span data-ttu-id="136eb-105">En este tema se muestra cómo establecer la información de estado de día.</span><span class="sxs-lookup"><span data-stu-id="136eb-105">This topic demonstrates how to set day state information.</span></span> <span data-ttu-id="136eb-106">El control de calendario mensual utiliza información de estado de día para determinar cómo dibuja determinados días dentro del control.</span><span class="sxs-lookup"><span data-stu-id="136eb-106">The month calendar control uses day state information to determine how it draws specific days within the control.</span></span>

<span data-ttu-id="136eb-107">Los controles de calendario mensual que usan los Estados de la compatibilidad con el estilo [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="136eb-107">Month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style support day states.</span></span> <span data-ttu-id="136eb-108">La información de estado de día se expresa como un tipo de datos de 32 bits, [**MONTHDAYSTATE**](monthdaystate.md).</span><span class="sxs-lookup"><span data-stu-id="136eb-108">Day state information is expressed as a 32-bit data type, [**MONTHDAYSTATE**](monthdaystate.md).</span></span> <span data-ttu-id="136eb-109">Cada bit de un campo de bits de **MONTHDAYSTATE** (de 0 a 30) especifica el estado de un día de un mes.</span><span class="sxs-lookup"><span data-stu-id="136eb-109">Each bit in a **MONTHDAYSTATE** bitfield (0 through 30) specifies the state of a day in a month.</span></span> <span data-ttu-id="136eb-110">Si un bit está activado, el día correspondiente se muestra en negrita.</span><span class="sxs-lookup"><span data-stu-id="136eb-110">If a bit is on, the corresponding day is displayed in bold.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="136eb-111">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="136eb-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="136eb-112">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="136eb-112">Technologies</span></span>

-   [<span data-ttu-id="136eb-113">Controles de Windows</span><span class="sxs-lookup"><span data-stu-id="136eb-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="136eb-114">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="136eb-114">Prerequisites</span></span>

-   <span data-ttu-id="136eb-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="136eb-115">C/C++</span></span>
-   <span data-ttu-id="136eb-116">Programación de la interfaz de usuario de Windows</span><span class="sxs-lookup"><span data-stu-id="136eb-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="136eb-117">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="136eb-117">Instructions</span></span>


<span data-ttu-id="136eb-118">Una aplicación puede establecer explícitamente la información de estado de los días mediante el envío del mensaje de [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) o mediante la macro correspondiente, [**MonthCal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span><span class="sxs-lookup"><span data-stu-id="136eb-118">An application can explicitly set day state information by sending the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message or by using the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="136eb-119">Sin embargo, la información de estado de día normalmente se establece en respuesta al código de notificación [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , que se envía cada vez que es necesario actualizar el control porque, por ejemplo, se ha desplazado un mes diferente a la vista.</span><span class="sxs-lookup"><span data-stu-id="136eb-119">However, day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed because, for example, a different month has scrolled into view.</span></span>

<span data-ttu-id="136eb-120">En el ejemplo de código siguiente se muestra cómo procesar el código de notificación [MCN \_ GETDAYSTATE](mcn-getdaystate.md) en un controlador de mensajes de [**\_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="136eb-120">The following example code shows how to process the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code in a [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="136eb-121">Procesa MCN \_ GETDAYSTATE especificando que debe resaltarse el primer y el decimoquinto día de cada mes visible.</span><span class="sxs-lookup"><span data-stu-id="136eb-121">It processes MCN\_GETDAYSTATE by specifying that the first and fifteenth day of each visible month should be highlighted.</span></span> <span data-ttu-id="136eb-122">El miembro **cDayState** de la estructura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) especifica el número de valores [**MONTHDAYSTATE**](monthdaystate.md) que se necesitan en la matriz, que recibe un tamaño máximo arbitrario.</span><span class="sxs-lookup"><span data-stu-id="136eb-122">The **cDayState** member of the [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure specifies the number of [**MONTHDAYSTATE**](monthdaystate.md) values that are needed in the array, which is given an arbitrary maximum size.</span></span> <span data-ttu-id="136eb-123">A continuación, el código recorre en bucle para establecer los bits adecuados en cada elemento válido de la matriz mediante la macro **BOLDDAY** definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="136eb-123">The code then loops to set the appropriate bits in each valid element of the array, using the application-defined **BOLDDAY** macro.</span></span>



```C++
    #define BOLDDAY(ds, iDay)  \
        if (iDay > 0 && iDay < 32)(ds) |= (0x00000001 << (iDay - 1))

    case WM_NOTIFY:
            if (((LPNMHDR)lParam)->code == MCN_GETDAYSTATE)
            {
                MONTHDAYSTATE rgMonths[12] = { 0 };
                int cMonths = ((NMDAYSTATE*)lParam)->cDayState;
                for (int i = 0; i < cMonths; i++)
                {
                    BOLDDAY(rgMonths[i], 1);
                    BOLDDAY(rgMonths[i], 15);
                }
                ((NMDAYSTATE*)lParam)->prgDayState = rgMonths;
                return TRUE;
            }
            break;
```



## <a name="related-topics"></a><span data-ttu-id="136eb-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="136eb-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="136eb-125">Referencia de control de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="136eb-125">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="136eb-126">Acerca de los controles de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="136eb-126">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="136eb-127">Usar controles de calendario mensual</span><span class="sxs-lookup"><span data-stu-id="136eb-127">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 




