---
description: En el ejemplo siguiente se muestra cómo crear un cuadro de mensaje condicional que aparece y advierte al usuario de que una tarea en segundo plano se sigue ejecutando cada vez que el usuario activa un control mostrado prematuramente.
ms.assetid: 4a99a96b-50c2-42eb-82ad-acdfa186a71f
title: Creación de un "Please Wait . . ." Cuadro de mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5f0cb1e4f1a0224c3b71d42d6fc63c1940483
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159054"
---
# <a name="authoring-a-conditional-please-wait-message-box"></a>Creación de un condicional "Please Wait..." Cuadro de mensaje

En el ejemplo siguiente se muestra cómo crear un cuadro de mensaje condicional que aparece y advierte al usuario de que una tarea en segundo plano se sigue ejecutando cada vez que el usuario activa un control mostrado prematuramente.

En el ejemplo también se muestra cómo [spawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) se puede usar generalmente para proteger un control que desencadena una acción dependiente de la finalización de una tarea en segundo plano.

En este ejemplo, se muestra al usuario durante el proceso  de instalación un cuadro de diálogo de selección que contiene tres controles de botón de inserción con las etiquetas Instalar **ahora,** Siguiente y Costo de disco. [](selection-dialog.md) Sin embargo, el instalador también lleva a cabo una tarea de costo de espacio en disco en segundo plano mientras se muestra este cuadro de diálogo. El autor desea proteger estos botones de la activación y quiere que se active un cuadro de mensaje "Please wait" (Espere por favor) si el usuario hace clic en cualquiera de los botones antes de que se haya completado el costo. El autor también quiere que este cuadro de mensaje contenga un **botón Cancelar** y que desaparezca en cuanto finalice la tarea en segundo plano.

**Para mostrar un cuadro de diálogo en el que se pide al usuario que espere mientras se completa el costo del disco en segundo plano**

1.  Use las funcionalidades de creación del instalador para agregar un nuevo cuadro de diálogo modal denominado **WaitForCosting** a la [tabla Dialog](dialog-table.md). El cuadro de diálogo debe mostrar una cadena de texto que dice "Espere mientras se complete el costo del espacio en disco".
2.  Agregue un único control de botón de inserción a este cuadro de diálogo, con la etiqueta **Cancelar**, mediante su creación en la [tabla Control](control-table.md).
3.  Vincule **el botón** de inserción Cancelar a un control ControlEvent que cierre el cuadro de diálogo **WaitForCosting** mediante la creación de [un control EndDialog ControlEvent](enddialog-controlevent.md) en la [tabla ControlEvent](controlevent-table.md). Establezca el argumento del evento EndDialog Control en Exit.
4.  Vincule [un elemento SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md) a los controles de botón de inserción Install **Now**, **Next** y **Disk Cost** existentes que se muestran en el cuadro de diálogo [Selección.](selection-dialog.md) Establezca el argumento de este controlEvent en la tabla ControlEvent para que sea el cuadro de diálogo **WaitForCosting** y establezca la expresión en la columna Condición de la tabla para que sea: [**CostingComplete**](costingcomplete.md) =1.

 

 



