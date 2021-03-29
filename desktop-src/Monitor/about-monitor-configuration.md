---
title: Acerca de la configuración de monitor
description: Acerca de la configuración de monitor
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- supervisar, acerca de
- supervisión, calibración de color
- monitor, ajuste del área de visualización del monitor
- supervisar, guardar la configuración del monitor
- supervisar, restaurar la configuración de monitor
- supervisión, características de proveedor
- calibración de color
- ajustar el área de visualización del monitor
- guardar la configuración del monitor
- restaurar la configuración del monitor
- características del proveedor
- configuración del monitor, calibración de color
- supervisión de la configuración, acerca de
- configuración del monitor, ajuste del área de visualización del monitor
- supervisar la configuración, guardar la configuración del monitor
- supervisión de la configuración, restauración de la configuración de monitor
- configuración de supervisión, características de proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d8e2f3d463bc84acaf8b48f493f5a0118976ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532067"
---
# <a name="about-monitor-configuration"></a>Acerca de la configuración de monitor

Los usos de las funciones de configuración del monitor incluyen:

-   Calibración de color. Un monitor calibrado correctamente reproduce los colores correctamente. Normalmente, una aplicación de calibración de color muestra un patrón de prueba y tiene controles para cambiar la configuración de un monitor. El usuario cambia la configuración hasta que se cumple una condición y repite este proceso para cada configuración del monitor hasta que se calibra el monitor.
-   Ajuste del área de visualización del monitor. Las funciones de configuración del monitor se pueden usar para cambiar el tamaño y la posición del área de presentación de un monitor. Por ejemplo, cuando un monitor LCD está conectado a un equipo mediante un conector analógico, se obtiene la mejor calidad de imagen cuando hay una asignación de uno a uno entre píxeles en el búfer de fotogramas de la tarjeta gráfica y píxeles en el monitor LCD.
-   Guardar y restaurar la configuración del monitor. Algunos usuarios necesitan varios conjuntos de valores de supervisión, ya que los distintos escenarios requieren una configuración de monitor diferente. Por ejemplo, la configuración de supervisión que es óptima para las aplicaciones de escritorio no es óptima para ver la televisión.
-   Usar las características de supervisión específicas del proveedor. Con las funciones de configuración del monitor, los fabricantes pueden crear aplicaciones que usen las características específicas del proveedor del monitor.

Las funciones de configuración del monitor se dividen en funciones de alto nivel y bajo nivel. Las funciones de alto nivel son más fáciles de usar que las funciones de bajo nivel. Para usar las funciones de alto nivel, no es necesario saber nada sobre la interfaz de comandos del canal de datos de pantalla (DDC/CI). Sin embargo, las funciones de alto nivel no proporcionan acceso a las características específicas del proveedor del monitor.

Las funciones de bajo nivel son un contenedor fino en torno a los comandos DDC/CI. Para usar las funciones de bajo nivel, debe estar familiarizado con el estándar DDC/CI y también con el estándar del conjunto de comandos de control de monitor de VESA (MCCS). Por lo general, debe usar las funciones de alto nivel a menos que necesite usar características que solo están disponibles en las funciones de bajo nivel.

Las funciones de configuración del monitor de alto nivel están diseñadas para que una aplicación no pueda poner un monitor en un estado inutilizable. Las funciones de bajo nivel se pueden usar para enviar códigos VCP al monitor. Sin embargo, tenga en cuenta que algunos códigos VCP pueden deshabilitar la funcionalidad importante o poner el monitor en un estado en el que el usuario no pueda ver la imagen de la pantalla. Para obtener más información, consulte el estándar del conjunto de comandos de control de monitor de VESA (MCCS).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de monitor](monitor-configuration.md)
</dt> </dl>

 

 




