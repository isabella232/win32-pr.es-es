---
description: En el ejemplo siguiente se muestra cómo crear un cuadro de mensaje condicional que emerge y advierte al usuario de que se está ejecutando una tarea en segundo plano cada vez que el usuario activa un control mostrado prematuramente.
ms.assetid: 4a99a96b-50c2-42eb-82ad-acdfa186a71f
title: Crear un "espere. . ." Cuadro de mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5f0cb1e4f1a0224c3b71d42d6fc63c1940483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545179"
---
# <a name="authoring-a-conditional-please-wait-message-box"></a>Creación de una instrucción condicional "espere...." Cuadro de mensaje

En el ejemplo siguiente se muestra cómo crear un cuadro de mensaje condicional que emerge y advierte al usuario de que se está ejecutando una tarea en segundo plano cada vez que el usuario activa un control mostrado prematuramente.

En el ejemplo también se muestra cómo [SpawnWaitDialog ControlEvent,](spawnwaitdialog-controlevent.md) se puede utilizar generalmente para proteger un control que desencadena una acción dependiente de la finalización de una tarea en segundo plano.

En este ejemplo, se muestra al usuario un [cuadro de diálogo de selección](selection-dialog.md) que contiene tres controles de botón de control con la etiqueta **instalar ahora**, **siguiente** y **costo del disco** durante el proceso de instalación. Sin embargo, el instalador también realiza una tarea de costo de espacio en disco en segundo plano al mostrar este cuadro de diálogo. El autor desea proteger estos botones de la activación y desea que aparezca un cuadro de mensaje "Espere" si el usuario hace clic en cualquiera de los botones antes de que se haya completado el costo. El autor también desea que este cuadro de mensaje contenga un botón **Cancelar** y que desaparezca en cuanto termine la tarea en segundo plano.

**Para mostrar un cuadro de diálogo que pide al usuario que espere mientras se completa el costo del disco en segundo plano**

1.  Use las capacidades de creación del instalador para agregar un nuevo cuadro de diálogo modal, denominado **WaitForCosting**, en la [tabla del cuadro de diálogo](dialog-table.md). El cuadro de diálogo debe mostrar una cadena de texto que indica "espere a que se complete el costo de espacio en disco".
2.  Agregue un control de botón de control único a este cuadro de diálogo, etiquetado como **Cancelar**, mediante su creación en la [tabla de control](control-table.md).
3.  Vincule el botón de **cancelación** de la extracción a un ControlEvent, que cierre el cuadro de diálogo **WaitForCosting** mediante la creación de un [ControlEvent, EndDialog](enddialog-controlevent.md) en la [tabla ControlEvent,](controlevent-table.md). Establezca el argumento del evento de control EndDialog en Exit.
4.  Vincular [un ControlEvent, de SpawnWaitDialog](spawnwaitdialog-controlevent.md) a los controles de botón de **instalación instalar ahora**, **siguiente** y **costo del disco** que se muestran en el cuadro de [diálogo Selección](selection-dialog.md) . Establezca el argumento de este ControlEvent, en la tabla ControlEvent, en el cuadro de diálogo **WaitForCosting** y establezca la expresión de la columna condición de la tabla en: [**CostingComplete**](costingcomplete.md) = 1.

 

 



