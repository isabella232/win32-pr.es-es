---
title: Acerca de la configuración del monitor
description: Acerca de la configuración del monitor
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- monitor,about
- monitor,calibración de color
- monitor, ajustar el área de visualización del monitor
- monitor, guardar la configuración del monitor
- monitor, restaurar la configuración del monitor
- monitor,características del proveedor
- calibración de color
- ajustar el área de visualización del monitor
- guardar la configuración del monitor
- restaurar la configuración del monitor
- características del proveedor
- supervisar la configuración, calibración de color
- supervisar la configuración, acerca de
- configuración de monitor, ajustar el área de visualización del monitor
- configuración de monitor, guardar la configuración del monitor
- supervisar la configuración, restaurar la configuración del monitor
- supervisar la configuración, características del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5f3d8c56521c07d704fe586f486298d0e679d1bfc33e25a29d943aa92dd66e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146188"
---
# <a name="about-monitor-configuration"></a>Acerca de la configuración del monitor

Entre los usos de las funciones de configuración del monitor se incluyen:

-   Calibración del color. Un monitor calibrado correctamente reproduce los colores correctamente. Normalmente, una aplicación de calibración de color muestra un patrón de prueba y tiene controles para cambiar una configuración de monitor. El usuario cambia la configuración hasta que se cumple una condición y repite este proceso para cada configuración de monitor hasta que se calibra el monitor.
-   Ajustar el área de visualización del monitor. Las funciones de configuración del monitor se pueden usar para cambiar el tamaño y la posición del área de presentación de un monitor. Por ejemplo, cuando se conecta un monitor DEFI A A a un equipo mediante un conector análogo, se obtiene la mejor calidad de imagen cuando hay una asignación uno a uno entre píxeles en el búfer de fotogramas de la tarjeta gráfica y píxeles en el monitor DEFI.
-   Guardar y restaurar la configuración del monitor. Algunos usuarios necesitan varios conjuntos de configuraciones de supervisión, ya que distintos escenarios requieren diferentes configuraciones de supervisión. Por ejemplo, la configuración de supervisión que es óptima para las aplicaciones de escritorio no es óptima para ver televisión.
-   Uso de características de supervisión específicas del proveedor. Con las funciones de configuración de supervisión, los fabricantes pueden crear aplicaciones que usen las características específicas del proveedor del monitor.

Las funciones de configuración del monitor se dividen en funciones de alto y bajo nivel. Las funciones de alto nivel son más fáciles de usar que las funciones de bajo nivel. Para usar las funciones de alto nivel, no es necesario saber nada sobre la interfaz de comandos del canal de datos para mostrar (DDC/CI). Sin embargo, las funciones de alto nivel no le dan acceso a las características específicas del proveedor del monitor.

Las funciones de bajo nivel son un contenedor fino alrededor de los comandos DDC/CI. Para usar las funciones de bajo nivel, debe estar familiarizado con el estándar DDC/CI y también con el estándar vesA Monitor Control Command Set (MCCS). Por lo general, debe usar las funciones de alto nivel a menos que tenga que usar características que solo están disponibles en las funciones de bajo nivel.

Las funciones de configuración de supervisión de alto nivel están diseñadas para que una aplicación no pueda poner un monitor en un estado inutilizable. Las funciones de bajo nivel se pueden usar para enviar códigos VCP al monitor. Sin embargo, tenga en cuenta que algunos códigos VCP pueden deshabilitar la funcionalidad importante o poner el monitor en un estado en el que el usuario no pueda ver la imagen para mostrar. Para más información, consulte el estándar VESA Monitor Control Command Set (MCCS).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión de la configuración](monitor-configuration.md)
</dt> </dl>

 

 




