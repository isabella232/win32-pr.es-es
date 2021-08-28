---
title: Acerca de los controles de calendario mensual
description: Un control de calendario mensual implementa una interfaz de usuario de tipo calendario.
ms.assetid: 81b8f233-272e-4043-92ff-5ff47b0610d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72000e0cecbfe627068260c5d9263821437246c15bebdfb876ecaa84e61f9cda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834530"
---
# <a name="about-month-calendar-controls"></a>Acerca de los controles de calendario mensual

Un control de calendario mensual implementa una interfaz de usuario de tipo calendario. Esto proporciona al usuario un método muy intuitivo y reconocible para especificar o seleccionar una fecha. El control también proporciona a la aplicación los medios para obtener y establecer la información de fecha en el control mediante tipos de datos existentes.

-   [Características de control de calendario mensual](#month-calendar-control-features)
    -   [Selección de un día](#selecting-a-day)
    -   [Selección de un mes no próximo](#selecting-a-nonadjacent-month)
    -   [Selección de un año diferente](#selecting-a-different-year)
-   [Localización](#localization)
-   [Horas del control Calendario mensual](#times-in-the-month-calendar-control)

## <a name="month-calendar-control-features"></a>Características de control de calendario mensual

En la siguiente captura de pantalla se muestra un control de calendario mensual que se ha dimensionado para mostrar dos meses.

![captura de pantalla de un cuadro de diálogo con un control de calendario mensual que muestra dos meses, en paralelo](images/mc-simple.png)

> [!Note]  
> La apariencia y el comportamiento del control de calendario mensual difiere ligeramente en las distintas versiones de la biblioteca en tiempo de ejecución. Este tema se centra en el control tal como aparece en Windows Vista con la versión 6 de Comctl32.dll.

 

El control de la ilustración tiene las siguientes características opcionales.

-   La fecha actual se muestra en una línea independiente en la parte inferior del control. Éste es el estilo predeterminado.
-   El "círculo de hoy" (en realidad un rectángulo en esta versión) aparece alrededor del día actual y junto a la línea "Hoy" como una indicación visual. Éste es el estilo predeterminado.
-   Los números de semana se muestran a la izquierda de cada fila de días. Se debe especificar este estilo.
-   Algunas fechas se muestran en negrita, según el estado de día establecido por la aplicación. Por ejemplo, las fechas que tienen reuniones programadas se pueden mostrar en negrita. Se debe especificar este estilo.

> [!Note]
>
> Windows no admite fechas anteriores a la 1601. Consulte [**FILETIME para**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) obtener más información.
>
> El control de calendario mensual se basa en el calendario gregoriano, que se introdujo en 1753. No calculará las fechas coherentes con el calendario de Maya que estaba en uso antes de 1753.

 

### <a name="selecting-a-day"></a>Selección de un día

De forma predeterminada, cuando un usuario hace clic en los botones de flecha de la parte superior izquierda o superior derecha del control de calendario mensual, el control actualiza su presentación para mostrar el mes anterior o el siguiente. El usuario también puede realizar la misma acción haciendo clic en los meses parciales mostrados antes del primer mes y después del último mes.

Los siguientes comandos de teclado también se pueden usar para mover la selección. El calendario siempre se desplaza según sea necesario para mostrar el día seleccionado. (Los [**códigos de clave virtual**](/windows/desktop/inputdev/virtual-key-codes) se muestran en la tabla).



|    Comando      |    Descripción                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flecha izquierda (VK \_ LEFT)   | Seleccione el día anterior.                                                                                                                                                                                                                 |
| Flecha derecha (VK \_ RIGHT) | Seleccione el día siguiente.                                                                                                                                                                                                                     |
| Flecha arriba (VK \_ UP)       | Seleccione el mismo día de la semana anterior.                                                                                                                                                                                                |
| Flecha abajo (VK \_ DOWN)   | Seleccione el mismo día de la semana siguiente.                                                                                                                                                                                                    |
| PAGE UP (VK \_ PRIOR)     | Seleccione el mismo día del mes anterior. (Si ese mes no tiene el día, se selecciona el día más cercano; por ejemplo, la selección pasa del 31 de marzo al 28 o 29 de febrero).                                                      |
| PÁGINA ABAJO (SIGUIENTE \_ VK)    | Seleccione el mismo día del mes siguiente.                                                                                                                                                                                                   |
| HOME (VK \_ HOME)         | Seleccione el primer día del mes actual.                                                                                                                                                                                               |
| END (VK \_ END)           | Seleccione el último día del mes actual.                                                                                                                                                                                                |
| CTRL + INICIO             | Desplácese un mes hacia atrás y seleccione un día en la columna situada más a la izquierda.                                                                                                                                                                       |
| CTRL + FINAL              | Desplácese un mes hacia delante y seleccione un día en la columna situada más a la derecha.                                                                                                                                                                       |
| CTRL + SUBIR PÁGINA          | Seleccione el mismo día de un mes anterior. El número de meses por los que se mueve la selección es el número de meses que se muestran en el control. Por ejemplo, si se muestran dos meses, la selección se movería del 6 de junio al 6 de mayo.    |
| CTRL + BAJAR PÁGINA        | Seleccione el mismo día de un mes anterior. El número de meses por los que se mueve la selección es el número de meses que se muestran en el control. Por ejemplo, si se muestran dos meses, la selección se movería del 6 de junio al 6 de agosto. |



 

Si un control de calendario mensual no usa el estilo [**\_ NOTODAY de MCS,**](month-calendar-control-styles.md) el usuario puede volver al día actual haciendo clic en el texto "Hoy" en la parte inferior del control. Si el día actual no está visible, el control actualiza su presentación para mostrarlo.

Una aplicación puede cambiar el número de meses en los que el control actualiza su presentación mediante el mensaje [**\_ SETMONTHDELTA**](mcm-setmonthdelta.md) de MCM o la macro correspondiente, [**MonthCal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta). Sin embargo, las claves PAGE UP y PAGE DOWN cambian el mes seleccionado en uno, independientemente del número de meses mostrados o del valor establecido por **MCM \_ SETMONTHDELTA.**

### <a name="selecting-a-nonadjacent-month"></a>Selección de un mes no próximo

Cuando un usuario hace clic en el nombre de un mes mostrado, se muestran todos los meses del año (en versiones anteriores, se trata de un menú emergente). El usuario puede seleccionar un mes en la lista. Si la selección del usuario no está visible, el control de calendario mensual se desplaza por su pantalla para mostrar el mes elegido. En la siguiente captura de pantalla, un control de calendario mensual muestra los meses de dos años adyacentes.

![captura de pantalla de un cuadro de diálogo con un control de calendario mensual que muestra todos los meses de 2007 y 2008](images/mc-months.png)

### <a name="selecting-a-different-year"></a>Selección de un año diferente

Si el usuario hace clic en el año, aparece un grupo de años y el usuario puede seleccionar uno diferente, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de un control de calendario mensual que muestra todos los años de 1999 a 2020](images/mc-years.png)

## <a name="localization"></a>Localización

El control month-calendar obtiene su formato y todas las cadenas de LOCALE \_ USER \_ DEFAULT.

## <a name="times-in-the-month-calendar-control"></a>Horas del control Calendario mensual

El control de calendario mensual no muestra la hora. Sin embargo, la [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que se usa para establecer y recuperar la fecha seleccionada o la fecha actual contiene campos de hora. Cuando se establece una fecha mediante programación, el control copia los campos de hora tal y como están o los valida primero y, después, si no son válidos, almacena las horas predeterminadas actuales. A continuación se muestra una lista de los mensajes que establecen una fecha y una descripción de cómo se tratan los campos de hora.



|  Message         |  Descripción            |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCM \_ SETCURSEL**](mcm-setcursel.md)     | El control copia los campos de tiempo tal como están, sin validación ni modificación.                                                                                                                                        |
| [**MCM \_ SETRANGE**](mcm-setrange.md)       | Se validan los campos de tiempo de las estructuras pasadas. Si son válidos, los campos de hora se copian sin modificaciones. Si no son válidos, el control copia los campos de tiempo de los datos actuales.                  |
| [**MCM \_ SETSELRANGE**](mcm-setselrange.md) | Se validan los campos de tiempo de las estructuras pasadas. Si son válidos, los campos de hora se copian sin modificaciones. Si no son válidas, el control conserva los campos de tiempo de los intervalos de selección actuales. |
| [**MCM \_ SETTODAY**](mcm-settoday.md)       | El control copia los campos de tiempo tal como están, sin validación ni modificación.                                                                                                                                        |



 

Cuando se recupera una fecha del control , los campos de hora se copiarán de las horas almacenadas sin modificaciones. El control de los campos de tiempo por parte del control se proporciona como una comodidad para el programador. El control no examina ni modifica los campos de tiempo como resultado de ninguna operación que no sea la enumerada anteriormente.

 

 