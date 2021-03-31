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
# <a name="how-to-set-day-states"></a>Establecimiento de los Estados de día

En este tema se muestra cómo establecer la información de estado de día. El control de calendario mensual utiliza información de estado de día para determinar cómo dibuja determinados días dentro del control.

Los controles de calendario mensual que usan los Estados de la compatibilidad con el estilo [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) . La información de estado de día se expresa como un tipo de datos de 32 bits, [**MONTHDAYSTATE**](monthdaystate.md). Cada bit de un campo de bits de **MONTHDAYSTATE** (de 0 a 30) especifica el estado de un día de un mes. Si un bit está activado, el día correspondiente se muestra en negrita.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Una aplicación puede establecer explícitamente la información de estado de los días mediante el envío del mensaje de [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) o mediante la macro correspondiente, [**MonthCal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Sin embargo, la información de estado de día normalmente se establece en respuesta al código de notificación [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , que se envía cada vez que es necesario actualizar el control porque, por ejemplo, se ha desplazado un mes diferente a la vista.

En el ejemplo de código siguiente se muestra cómo procesar el código de notificación [MCN \_ GETDAYSTATE](mcn-getdaystate.md) en un controlador de mensajes de [**\_ notificación de WM**](wm-notify.md) . Procesa MCN \_ GETDAYSTATE especificando que debe resaltarse el primer y el decimoquinto día de cada mes visible. El miembro **cDayState** de la estructura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) especifica el número de valores [**MONTHDAYSTATE**](monthdaystate.md) que se necesitan en la matriz, que recibe un tamaño máximo arbitrario. A continuación, el código recorre en bucle para establecer los bits adecuados en cada elemento válido de la matriz mediante la macro **BOLDDAY** definida por la aplicación.



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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de control de calendario mensual](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[Acerca de los controles de calendario mensual](month-calendar-controls.md)
</dt> <dt>

[Usar controles de calendario mensual](using-month-calendar-controls.md)
</dt> </dl>

 

 




