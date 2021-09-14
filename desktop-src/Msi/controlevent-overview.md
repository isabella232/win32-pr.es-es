---
description: Los controlEvents son análogos a los mensajes Windows microsoft en aplicaciones basadas en Win32.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Información general de ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158770"
---
# <a name="controlevent-overview"></a>Información general de ControlEvent

Los controlEvents son análogos a los mensajes Windows microsoft en aplicaciones basadas en Win32. Sin embargo, en lugar de crear una función de devolución de llamada para recibir mensajes Windows y enviar mensajes Windows con la [función SendMessage,](/windows/win32/api/winuser/nf-winuser-sendmessage) el instalador de la interfaz de usuario (UI) y los controles publican [ControlEvents](control-events.md). Se pueden especificar otros controles y el instalador para suscribirse a determinados ControlEvents que, a continuación, cambiarán los atributos del control de suscripción. Para agregar controles de trabajo a los cuadros de diálogo, el autor de la interfaz de usuario especifica la publicación de ControlEvents en la [tabla ControlEvent](controlevent-table.md) y suscribe los controles a ControlEvents en la [tabla EventMapping](eventmapping-table.md).

El instalador publicará los siguientes eventos en los controles de suscripción enumerados en la [tabla EventMapping](eventmapping-table.md). Normalmente, [un control ProgressBar](progressbar-control.md) [o Un control Descríba](billboard-control.md) se suscribe a SetProgress; el resto se suscriben mediante controles [Text.](text-control.md)

[ActionData ControlEvent](actiondata-controlevent.md)

[ActionText ControlEvent](actiontext-controlevent.md)

[SetProgress ControlEvent](setprogress-controlevent.md)

[TimeRemaining ControlEvent](timeremaining-controlevent.md)

[ScriptInProgress ControlEvent](scriptinprogress-controlevent.md)

El control publica los siguientes eventos cuando la selección de elementos se mueve en un [control SelectionTree](selectiontree-control.md) o [directoryList Control](directorylist-control.md). Los controles de suscripción deben encontrarse en el mismo cuadro de diálogo y aparecer en la tabla EventMapping.

[IgnoreChange ControlEvent](ignorechange-controlevent.md)

[SelectionDescription ControlEvent](selectiondescription-controlevent.md)

[SelectionSize ControlEvent](selectionsize-controlevent.md)

[SelectionPath ControlEvent](selectionpath-controlevent.md)

[SelectionAction ControlEvent](selectionaction-controlevent.md)

[SelectionNoItems ControlEvent](selectionnoitems-controlevent.md)

Los siguientes controles ControlEvents se pueden publicar a discreción de un usuario mediante la interacción con un [control PushButton](pushbutton-control.md) o [un control CheckBox](checkbox-control.md) en un cuadro de diálogo. El control Checkbox solo puede publicar los eventos AddLocal, AddSource, Remove, DoAction y SetProperty. Con Windows Installer que se incluye con Windows Server 2003 y versiones posteriores, el [control SelectionTree](selectiontree-control.md) puede publicar los controles DoAction, ControlEvent y SetProperty ControlEvents. El autor de la interfaz de usuario debe enumerar el controlEvent en la [tabla ControlEvent](controlevent-table.md). El controlador de interfaz de usuario del instalador es el suscriptor de estos eventos.

[AddLocal ControlEvent](addlocal-controlevent.md)

[AddSource ControlEvent](addsource-controlevent.md)

[CheckExistingTargetPath ControlEvent](checkexistingtargetpath-controlevent.md)

[CheckTargetPath ControlEvent](checktargetpath-controlevent.md)

[DoAction ControlEvent](doaction-controlevent.md)

[EnableRollback ControlEvent](enablerollback-controlevent.md)

[EndDialog ControlEvent](enddialog-controlevent.md)

[NewDialog ControlEvent](newdialog-controlevent.md)

[Reinstalar ControlEvent](reinstall-controlevent.md)

[ReinstallMode ControlEvent](reinstallmode-controlevent.md)

[Quitar ControlEvent](remove-controlevent.md)

[Restablecer ControlEvent](reset-controlevent.md)

[SetInstallLevel ControlEvent](setinstalllevel-controlevent.md)

[SetProperty ControlEvent](setproperty-controlevent.md)

[SetTargetPath ControlEvent](settargetpath-controlevent.md)

[SpawnDialog ControlEvent](spawndialog-controlevent.md)

[SpawnWaitDialog ControlEvent](spawnwaitdialog-controlevent.md)

[ValidateProductID ControlEvent](validateproductid-controlevent.md)

Un [control PushButton](pushbutton-control.md) puede publicar los siguientes eventos en un [control SelectionTree](selectiontree-control.md) de suscripción o en un [control DirectoryList](directorylist-control.md) ubicado en el mismo cuadro de diálogo. El control PushButton debe aparecer en la tabla ControlEvent y los controles de suscripción deben aparecer en la tabla EventMapping.

[SelectionBrowse ControlEvent](selectionbrowse-controlevent.md)

[DirectoryListUp ControlEvent](directorylistup-controlevent.md)

[DirectoryListNew ControlEvent](directorylistnew-controlevent.md)

[DirectoryListOpen ControlEvent](directorylistopen-controlevent.md)

Por lo general, los eventos de control requieren que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. La mayoría de los controles [](r-gly.md) ControlEvents no funcionarán con una interfaz de usuario reducida o una interfaz de usuario básica [*porque*](b-gly.md) estos niveles solo muestran cuadros de diálogo de modelo. Los eventos ActionText, AddSource, SetProgress, TimeRemaining y ScriptInProgress son excepciones y funcionarán en una interfaz de usuario reducida o básica. Para obtener más información sobre los niveles de interfaz de [usuario, vea Interfaz de usuario niveles .](user-interface-levels.md)

Puede ejecutar acciones [personalizadas mediante](custom-actions.md) la publicación de un control ControlEvent desde un [control PushButton o](pushbutton-control.md) un control [Checkbox](checkbox-control.md). Agregue un registro a la [tabla ControlEvent](controlevent-table.md) con los nombres del cuadro de diálogo y el control que publica controlEvent. Este control debe publicar un [control DoAction ControlEvent](doaction-controlevent.md) que notifique al instalador que ejecute la acción personalizada. En Windows XP o sistemas anteriores, no se puede ejecutar una acción personalizada mediante la publicación de un control ControlEvent desde un [control SelectionTree](selectiontree-control.md).

Para obtener más información sobre determinados ControlEvents, vea la lista de [ControlEvents estándar](control-events.md) [en Interfaz de usuario Reference](user-interface-reference.md).

 

 
