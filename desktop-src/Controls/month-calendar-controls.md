---
title: Acerca de los controles de calendario mensual
description: Un control de calendario mensual implementa una interfaz de usuario similar a un calendario.
ms.assetid: 81b8f233-272e-4043-92ff-5ff47b0610d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f61b0ffc291473b330469910d1dad0317668e1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149662"
---
# <a name="about-month-calendar-controls"></a>Acerca de los controles de calendario mensual

Un control de calendario mensual implementa una interfaz de usuario similar a un calendario. Esto proporciona al usuario un método muy intuitivo y reconocible de escribir o seleccionar una fecha. El control también proporciona a la aplicación los medios para obtener y establecer la información de fecha en el control usando los tipos de datos existentes.

-   [Características del control de calendario mensual](#month-calendar-control-features)
    -   [Seleccionar un día](#selecting-a-day)
    -   [Seleccionar un mes no adyacente](#selecting-a-nonadjacent-month)
    -   [Seleccionar un año diferente](#selecting-a-different-year)
-   [Localización](#localization)
-   [Horas en el control de calendario mensual](#times-in-the-month-calendar-control)

## <a name="month-calendar-control-features"></a>Características del control de calendario mensual

En la captura de pantalla siguiente se muestra un control de calendario mensual cuyo tamaño se ha ajustado para mostrar dos meses.

![captura de pantalla de un cuadro de diálogo con un control de calendario mensual que muestra dos meses, en paralelo](images/mc-simple.png)

> [!Note]  
> La apariencia y el comportamiento del control de calendario mensual difieren ligeramente en las distintas versiones de la biblioteca en tiempo de ejecución. Este tema se centra en el control tal como aparece en Windows Vista con la versión 6 de Comctl32.dll.

 

El control de la ilustración tiene las siguientes características opcionales.

-   La fecha actual se muestra en una línea independiente en la parte inferior del control. Éste es el estilo predeterminado.
-   El "círculo de hoy" (realmente un rectángulo en esta versión) aparece alrededor del día actual y junto a la línea "hoy" como una indicación visual. Éste es el estilo predeterminado.
-   Los números de semana se muestran a la izquierda de cada fila de días. Se debe especificar este estilo.
-   Algunas fechas se muestran en negrita, según el estado de día establecido por la aplicación. Por ejemplo, las fechas que tienen reuniones programadas se pueden mostrar en negrita. Se debe especificar este estilo.

> [!Note]
>
> Windows no admite fechas anteriores a 1601. Consulte [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) para obtener más información.
>
> El control de calendario mensual se basa en el calendario gregoriano, que se presentó en 1753. No calculará fechas coherentes con el calendario juliano que estaba en uso antes de 1753.

 

### <a name="selecting-a-day"></a>Seleccionar un día

De forma predeterminada, cuando un usuario hace clic en los botones de flecha en la parte superior izquierda o superior derecha del control de calendario mensual, el control actualiza su presentación para mostrar el mes anterior o el siguiente. El usuario también puede realizar la misma acción haciendo clic en los meses parciales que aparecen antes del primer mes y después del último mes.

También se pueden usar los siguientes comandos de teclado para desplace la selección. El calendario siempre se desplaza según sea necesario para mostrar el día seleccionado. (Los [**códigos de tecla virtual**](/windows/desktop/inputdev/virtual-key-codes) se muestran en la tabla).



|                         |                                                                                                                                                                                                                                          |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flecha izquierda (VK \_ izquierda)   | Seleccione el día anterior.                                                                                                                                                                                                                 |
| Flecha derecha (VK \_ derecha) | Seleccione el día siguiente.                                                                                                                                                                                                                     |
| Flecha arriba (VK \_ arriba)       | Seleccione el mismo día de la semana anterior.                                                                                                                                                                                                |
| Flecha abajo (VK \_ abajo)   | Seleccione el mismo día de la semana siguiente.                                                                                                                                                                                                    |
| Re Pág (VK \_ anterior)     | Seleccione el mismo día del mes anterior. (Si ese mes no tiene el día, se selecciona el día más cercano; por ejemplo, la selección se mueve del 31 de marzo al 28 de febrero o 29).                                                      |
| Av Pág (VK \_ siguiente)    | Seleccione el mismo día en el mes siguiente.                                                                                                                                                                                                   |
| Inicio (VK \_ Home)         | Seleccione el primer día del mes actual.                                                                                                                                                                                               |
| END (VK \_ End)           | Seleccione el último día del mes actual.                                                                                                                                                                                                |
| CTRL + INICIO             | Desplazarse un mes hacia atrás y seleccionar un día en la columna situada más a la izquierda.                                                                                                                                                                       |
| CTRL + FIN              | Desplazarse un mes hacia delante y seleccionar un día en la columna situada más a la derecha.                                                                                                                                                                       |
| CTRL + RE PÁG          | Seleccione el mismo día en un mes anterior. El número de meses que se mueve la selección es el número de meses que se muestran en el control. Por ejemplo, si se muestran dos meses, la selección pasaría del 6 de junio al 6 de mayo.    |
| CTRL + AV PÁG        | Seleccione el mismo día en un mes anterior. El número de meses que se mueve la selección es el número de meses que se muestran en el control. Por ejemplo, si se muestran dos meses, la selección se desmoverá del 6 de junio al 6 de agosto. |



 

Si un control de calendario mensual no usa el estilo [**MCS \_ noactual**](month-calendar-control-styles.md) , el usuario puede volver al día actual haciendo clic en el texto "hoy" situado en la parte inferior del control. Si el día actual no está visible, el control actualiza su pantalla para mostrarlo.

Una aplicación puede cambiar el número de meses que el control actualiza su presentación mediante el mensaje de [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) o la macro correspondiente, [**MonthCal \_ SETMONTHDELTA**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta). Sin embargo, las teclas Re Pág y Av Pág cambian el mes seleccionado en uno, independientemente del número de meses que se muestren o del valor establecido por **MCM \_ SETMONTHDELTA**.

### <a name="selecting-a-nonadjacent-month"></a>Seleccionar un mes no adyacente

Cuando un usuario hace clic en el nombre de un mes que se muestra, se enumeran todos los meses del año (en versiones anteriores, se trata de un menú emergente). El usuario puede seleccionar un mes en la lista. Si la selección del usuario no está visible, el control de calendario mensual desplaza la pantalla para mostrar el mes elegido. En la siguiente captura de pantalla, un control de calendario mensual muestra los meses de dos años adyacentes.

![captura de pantalla de un cuadro de diálogo con un control de calendario mensual que muestra todos los meses de 2007 y 2008](images/mc-months.png)

### <a name="selecting-a-different-year"></a>Seleccionar un año diferente

Si el usuario hace clic en el año, se muestra un grupo de años y el usuario puede seleccionar uno diferente, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de un control de calendario mensual que muestra todos los años de 1999 a 2020](images/mc-years.png)

## <a name="localization"></a>Localización

El control de calendario mensual obtiene su formato y todas las cadenas de la configuración regional \_ predeterminada del usuario \_ .

## <a name="times-in-the-month-calendar-control"></a>Horas en el control de calendario mensual

El control de calendario mensual no muestra la hora. Sin embargo, la estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que se usa para establecer y recuperar la fecha seleccionada o la fecha de hoy contiene campos de hora. Cuando se establece una fecha mediante programación, el control copia los campos de tiempo tal como están o los valida primero y, a continuación, si no son válidos, almacena las horas predeterminadas actuales. A continuación se muestra una lista de los mensajes que establecen una fecha y una descripción de cómo se tratan los campos de hora.



|                                             |                                                                                                                                                                                                                            |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCM \_ SETCURSEL**](mcm-setcursel.md)     | El control copia los campos de hora como están, sin validación ni modificación.                                                                                                                                        |
| [**MCM \_ SetRange**](mcm-setrange.md)       | Se validan los campos de hora de las estructuras que se pasan. Si son válidos, los campos de hora se copian sin modificaciones. Si no son válidos, el control copia los campos de hora de los datos de hoy.                  |
| [**MCM \_ SETSELRANGE**](mcm-setselrange.md) | Se validan los campos de hora de las estructuras que se pasan. Si son válidos, los campos de hora se copian sin modificaciones. Si no son válidos, el control conserva los campos de tiempo de los intervalos de selección actuales. |
| [**MCM \_ SETTODAY**](mcm-settoday.md)       | El control copia los campos de hora como están, sin validación ni modificación.                                                                                                                                        |



 

Cuando se recupera una fecha del control, los campos de hora se copiarán de las horas almacenadas sin modificaciones. La administración de los campos de hora por el control se proporciona por comodidad al programador. El control no examina ni modifica los campos de hora como resultado de una operación distinta de las mencionadas anteriormente.

 

 