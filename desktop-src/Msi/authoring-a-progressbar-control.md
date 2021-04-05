---
description: Windows Installer contiene funcionalidad para mostrar un indicador de progreso en un cuadro de diálogo de presentación de acciones.
ms.assetid: cfc2d974-4f2d-4f52-9835-eab1dc091c9b
title: Crear un control ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b872ed2dd36fb8ed04ee48fd69e4680fce002a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909077"
---
# <a name="authoring-a-progressbar-control"></a>Crear un control ProgressBar

Windows Installer contiene funcionalidad para mostrar un indicador de progreso en un cuadro de diálogo de presentación de acciones. El [control ProgressBar](progressbar-control.md) representa gráficamente la instalación de componentes individuales e informa del tiempo total transcurrido con respecto al tiempo restante o del tiempo total aproximado restante hasta que se complete la instalación.

Para determinar el tiempo total previsto para la instalación, el instalador realiza un seguimiento de los tics de progreso totales previstos por cada acción durante la generación del script de ejecución. Una vez completada la generación del script, se almacena el total del paso de progreso y comienza la instalación.

Los mensajes de progreso que detallan el número transcurrido de TICs de progreso se envían al controlador de mensajes activo a medida que se ejecuta cada acción en el script. En cada mensaje de progreso, el instalador difunde un [SetProgress ControlEvent,](setprogress-controlevent.md) al cuadro de diálogo actualmente activo. La secuencia de la interfaz de usuario debe crearse para crear el cuadro de diálogo de visualización de la acción durante la ejecución del script para recibir los mensajes de ControlEvent, de SetProgress desde el instalador.

Cuando el cuadro de diálogo de visualización de la acción recibe un ControlEvent, SetProgress, comprueba la [tabla EventMapping](eventmapping-table.md) de los controles que se suscriben a la ControlEvent,. El control ProgressBar del cuadro de diálogo Mostrar acción se suscribe a con el atributo control de progreso especificado en la columna atributos. El atributo control de progreso especifica que el control ProgressBar pasará los valores "ticksSoFar" y "totalTicks" junto con SetProgress ControlEvent,. El control de barra de progreso utiliza esta información para avanzar la barra gráfica de izquierda a derecha para una instalación y de derecha a izquierda para una operación de [reversión](rollback-installation.md) .

Además, el instalador difunde un [ControlEvent, de TimeRemaining](timeremaining-controlevent.md) en cada mensaje de progreso. El tiempo total restante para la instalación se determina calculando primero la velocidad de ejecución, que es el número total de TICs transcurridos dividido por el tiempo total transcurrido desde que comenzó la instalación. Los tics totales que quedan divididos por la tasa de ejecución proporcionan el tiempo aproximado restante.

Cuando el cuadro de diálogo Mostrar acción recibe el ControlEvent, TimeRemaining, vuelve a buscar en la tabla EventMapping los controles que están suscritos. Para mostrar el tiempo restante, se debe suscribir un [control de texto](text-control.md) a TimeRemaining ControlEvent, con el atributo de [control TimeRemaining](timeremaining-control-attribute.md) especificado en la columna Attributes.

El control de texto suscrito consulta la [tabla UIText](uitext-table.md) para obtener una cadena de plantilla con parámetros denominada "TimeRemaining". Esta cadena tiene dos parámetros, \[ 1 \] para minutos y \[ 2 \] para segundos. El control de texto convierte cada valor en minutos y segundos, evalúa la cadena de plantilla TimeRemaining y actualiza el control de texto con la nueva información.

Si el nivel de presentación de la interfaz de usuario se establece en básico o inferior, el instalador muestra un cuadro de diálogo predeterminado que contiene una barra de progreso y un campo de texto TimeRemaining. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

 

 



