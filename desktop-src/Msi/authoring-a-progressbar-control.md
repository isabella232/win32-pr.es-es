---
description: Windows El instalador contiene la funcionalidad para mostrar un indicador de progreso en un cuadro de diálogo de presentación de acciones.
ms.assetid: cfc2d974-4f2d-4f52-9835-eab1dc091c9b
title: Creación de un control ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1074744220bde8734fe0cd1f65aa1037ff1f0cb26763a11845a7ea7f1b58e507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066165"
---
# <a name="authoring-a-progressbar-control"></a>Creación de un control ProgressBar

Windows El instalador contiene la funcionalidad para mostrar un indicador de progreso en un cuadro de diálogo de presentación de acciones. El [control ProgressBar](progressbar-control.md) representa gráficamente la instalación de componentes individuales e informa del tiempo total transcurrido en relación con el tiempo restante o el tiempo total aproximado restante hasta que se completa la instalación.

Para determinar el tiempo total previsto para la instalación, el instalador realiza un seguimiento de los tics de progreso totales previstos por cada acción durante la generación del script de ejecución. Una vez completada la generación de scripts, se almacena el total de la marca de progreso y comienza la instalación.

Los mensajes de progreso que detallan el número transcurrido de pasos de progreso se envían al controlador de mensajes activo a medida que se ejecuta cada acción del script. En cada mensaje de progreso, el instalador difunde [un control SetProgress ControlEvent](setprogress-controlevent.md) al cuadro de diálogo activo actualmente. Se debe crear la secuencia de interfaz de usuario para crear el cuadro de diálogo de presentación de la acción durante la ejecución del script para recibir los mensajes SetProgress ControlEvent del instalador.

Cuando el cuadro de diálogo de presentación de acciones recibe un control SetProgress ControlEvent, comprueba en la tabla [EventMapping](eventmapping-table.md) los controles que se suscriben al controlEvent. El control ProgressBar del cuadro de diálogo de presentación de la acción se suscribe con el atributo de control Progreso especificado en la columna Atributos . El atributo Progress Control especifica que se pasarán los valores "ticksSoFar" y "totalTicks" al control ProgressBar junto con SetProgress ControlEvent. El control de barra de progreso usa esta información para avanzar la barra gráfica de izquierda a derecha para una instalación y de derecha a izquierda para una [operación de reversión.](rollback-installation.md)

Además, el instalador difunde un [control ControlEvent de TimeRemaining](timeremaining-controlevent.md) en cada mensaje de progreso. El tiempo total restante para la instalación se determina calculando primero la tasa de ejecución, que es el número total de pasos transcurridos dividido por el tiempo total desde que se inició la instalación. El total de tics restantes divididos por la tasa de ejecución proporciona el tiempo aproximado restante.

Cuando el cuadro de diálogo de presentación de la acción recibe el control ControlEvent de TimeRemaining, busca de nuevo en la tabla EventMapping los controles suscritos. Para mostrar el tiempo restante, se debe suscribir un [control Text](text-control.md) al control TimeRemaining ControlEvent con el atributo de [control TimeRemaining](timeremaining-control-attribute.md) especificado en la columna Atributos.

El control Text suscrito consulta la tabla [UIText](uitext-table.md) para obtener una cadena de plantilla con parámetros denominada "TimeRemaining". Esta cadena tiene dos parámetros, \[ 1 \] para minutos y \[ 2 para \] segundos. El control Text convierte cada valor en minutos y segundos, evalúa la cadena de plantilla TimeRemaining y actualiza el control de texto con la nueva información.

Si el nivel de presentación de la interfaz de usuario se establece en básico o inferior, el instalador muestra un cuadro de diálogo predeterminado que contiene una barra de progreso y un campo de texto TimeRemaining. Para obtener más información, [vea Interfaz de usuario Levels](user-interface-levels.md).

 

 



