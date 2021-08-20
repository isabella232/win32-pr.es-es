---
title: Cómo establecer los estados de día
description: En este tema se muestra cómo establecer información de estado de día. El control de calendario mensual usa información de estado de día para determinar cómo dibuja días específicos dentro del control.
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3ed2c99e6faf18f0e1d06ec06eaaf9a0d573faebe6f3697e43562603447571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078479"
---
# <a name="how-to-set-day-states"></a>Cómo establecer los estados de día

En este tema se muestra cómo establecer información de estado de día. El control de calendario mensual usa información de estado de día para determinar cómo dibuja días específicos dentro del control.

Controles de calendario mensual que usan los estados de día de soporte del estilo [**\_ DAYSTATE de MCS.**](month-calendar-control-styles.md) La información de estado de día se expresa como un tipo de datos de 32 bits, [**MONTHDAYSTATE**](monthdaystate.md). Cada bit de un campo de bits **MONTHDAYSTATE** (de 0 a 30) especifica el estado de un día en un mes. Si un bit está en, el día correspondiente se muestra en negrita.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Una aplicación puede establecer explícitamente la información de estado del día mediante el envío del [**mensaje \_ SETDAYSTATE**](mcm-setdaystate.md) de MCM o mediante la macro correspondiente, [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Sin embargo, la información de estado de día normalmente se establece en respuesta al código de notificación [ \_ GETDAYSTATE de MCN,](mcn-getdaystate.md) que se envía siempre que se necesita actualizar el control porque, por ejemplo, se ha pasado a la vista un mes diferente.

El código de ejemplo siguiente muestra cómo procesar el código [de notificación \_ GETDAYSTATE](mcn-getdaystate.md) de MCN en un [**controlador de mensajes WM \_ NOTIFY.**](wm-notify.md) Procesa GETDAYSTATE de MCN especificando que se deben resaltar el primer y el decimoquinto día de cada mes \_ visible. El **miembro cDayState** de la estructura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) especifica el número de valores [**MONTHDAYSTATE**](monthdaystate.md) necesarios en la matriz, a la que se le asigna un tamaño máximo arbitrario. A continuación, el código recorre en bucle para establecer los bits adecuados en cada elemento válido de la matriz, mediante la macro **BOLDDAY** definida por la aplicación.



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

 

 




