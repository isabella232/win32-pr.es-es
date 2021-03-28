---
description: Cuando varios monitores forman parte del escritorio, los objetos pueden viajar sin problemas entre monitores.
ms.assetid: eb7576c6-322c-48d0-abbb-bdc3b34976c3
title: Acerca de varios monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5997e39768d01522ae1fdd2e976c611e67826350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984755"
---
# <a name="about-multiple-display-monitors"></a>Acerca de varios monitores de pantalla

Cuando varios monitores forman parte del escritorio, los objetos pueden viajar sin problemas entre monitores. Es decir, puede arrastrar ventanas o accesos directos de un monitor a otro, y puede ajustar el tamaño de las ventanas para que cubran más de un monitor. Además, si un monitor está instalado por encima de otro, aparece un cursor que deja la parte inferior del monitor superior en la parte superior del monitor inferior.

Normalmente, un usuario organiza los monitores del sistema para reflejar la organización de las unidades de visualización físicas; por ejemplo, en paralelo o una parte superior de la otra de la misma. El usuario lo hace con la pestaña monitores, que reemplaza la ficha **configuración** del cuadro de diálogo **propiedades de pantalla** a través del panel de control. Los monitores deben formar una región contigua, es decir, cada monitor toca a otro monitor en al menos una parte de un borde.

Cuando se mueve o se cambia el tamaño de una ventana, parte del título siempre es visible para que el usuario pueda moverla y cambiar el tamaño de la ventana con el mouse. El movimiento del cursor está restringido al área de los monitores, por lo que siempre está visible. Los iconos de Shell se colocan en el mismo monitor que la barra de tareas y la barra de tareas puede estar en cualquier monitor; consulte [varias consideraciones sobre el monitor para programas anteriores](multiple-monitor-considerations-for-older-programs.md).

Un sistema de varios monitores afecta a ciertas combinaciones de teclas. La combinación de teclas ALT + IMPRal toma una instantánea de la ventana de primer plano, como siempre. Sin embargo, la tecla Impr Pant toma una instantánea del monitor que tiene el mouse. La combinación de teclas CTRL + IMPRon toma una instantánea de toda la pantalla virtual, vea [la pantalla virtual](the-virtual-screen.md).

La compatibilidad con varios monitores no afecta al rendimiento de las aplicaciones cuando se ejecuta en un único entorno de presentación. Es decir, cuando se ejecuta en un único sistema de pantalla, no habrá ninguna sobrecarga adicional en el código de operaciones de gráficos de alto rendimiento. Sin embargo, en un sistema de varios monitores, el rendimiento se ve ligeramente afectado si una aplicación solo se ejecuta en uno de los dispositivos gráficos. Además, el rendimiento puede verse afectado en gran medida si una aplicación abarca varias pantallas, especialmente en el caso de las operaciones de uso intensivo de gráficos.

*Pantalla completa* es una característica proporcionada por el sistema operativo que permite al usuario alternar una aplicación en un estado especial en el que la aplicación puede tener acceso directamente al hardware de gráficos VGA. Se trata de una característica clave para juegos y otras aplicaciones orientadas a gráficos que requieren un alto rendimiento. Además, a menudo lo usan los desarrolladores para la edición de texto, ya que permite el desplazamiento de texto muy rápido.

En un entorno de varios monitores, solo un dispositivo gráfico puede ser compatible con VGA. Se trata de una limitación del hardware del equipo, que requiere que solo un dispositivo responda a cualquier dirección de hardware. Dado que el estándar de compatibilidad de hardware de VGA requiere direcciones de hardware específicas, solo puede haber un dispositivo de gráficos VGA en una máquina y solo este dispositivo puede responder físicamente a las direcciones VGA. Por lo tanto, las aplicaciones que requieran pasar a la pantalla completa solo se ejecutarán en el dispositivo concreto que admita la compatibilidad de hardware VGA.

En esta información general se proporciona información sobre los temas siguientes.

-   [La pantalla virtual](the-virtual-screen.md)
-   [HMONITOR y el contexto del dispositivo](hmonitor-and-the-device-context.md)
-   [Enumeración y control de visualización](enumeration-and-display-control.md)
-   [Varias métricas del sistema de supervisión](multiple-monitor-system-metrics.md)
-   [Usar varios monitores como pantallas independientes](using-multiple-monitors-as-independent-displays.md)
-   [Colores en varios monitores de pantalla](colors-on-multiple-display-monitors.md)
-   [Colocar objetos en varios monitores de pantalla](positioning-objects-on-multiple-display-monitors.md)
-   [Varias aplicaciones de supervisión en diferentes sistemas](multiple-monitor-applications-on-different-systems.md)
-   [Consideraciones de varios monitores para programas anteriores](multiple-monitor-considerations-for-older-programs.md)

 

 



