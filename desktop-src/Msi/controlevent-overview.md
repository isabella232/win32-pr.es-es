---
description: Los ControlEvents son análogos a los mensajes de Microsoft Windows en aplicaciones basadas en Win32.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Información general de ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913082"
---
# <a name="controlevent-overview"></a>Información general de ControlEvent,

Los ControlEvents son análogos a los mensajes de Microsoft Windows en aplicaciones basadas en Win32. Sin embargo, en lugar de crear una función de devolución de llamada para recibir mensajes de Windows y enviar mensajes de Windows con la función [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) , el instalador de la interfaz de usuario (IU) y los controles publican [ControlEvents](control-events.md). Se pueden especificar otros controles y el instalador para suscribirse a ControlEvents particulares que, a continuación, cambiarán los atributos del control de suscripción. Para agregar controles de trabajo a los cuadros de diálogo, el autor de la interfaz de usuario especifica la publicación de ControlEvents en la [tabla ControlEvent,](controlevent-table.md) y suscribe los controles a ControlEvents en la [tabla EventMapping](eventmapping-table.md).

El instalador publicará los siguientes eventos en los controles de suscripción que se enumeran en la [tabla EventMapping](eventmapping-table.md). Un control [ProgressBar](progressbar-control.md) o un [control](billboard-control.md) de la cartelera normalmente se suscribe a SetProgress, el resto se suscribe a por [los controles de texto](text-control.md).

[ActionData ControlEvent,](actiondata-controlevent.md)

[ActionText ControlEvent,](actiontext-controlevent.md)

[SetProgress ControlEvent,](setprogress-controlevent.md)

[TimeRemaining ControlEvent,](timeremaining-controlevent.md)

[ScriptInProgress ControlEvent,](scriptinprogress-controlevent.md)

El control publica los siguientes eventos cuando la selección de elementos se mueve en un control [SelectionTree](selectiontree-control.md) o [DirectoryList](directorylist-control.md). Los controles de suscripción deben estar ubicados en el mismo cuadro de diálogo y se muestran en la tabla EventMapping.

[IgnoreChange ControlEvent,](ignorechange-controlevent.md)

[SelectionDescription ControlEvent,](selectiondescription-controlevent.md)

[SelectionSize ControlEvent,](selectionsize-controlevent.md)

[SelectionPath ControlEvent,](selectionpath-controlevent.md)

[SelectionAction ControlEvent,](selectionaction-controlevent.md)

[SelectionNoItems ControlEvent,](selectionnoitems-controlevent.md)

Los siguientes ControlEvents se pueden publicar a la discreción de un usuario mediante la interacción con un [control de pulsador](pushbutton-control.md) o un [control de casilla](checkbox-control.md) en un cuadro de diálogo. El control CheckBox solo puede publicar los eventos AddLocal, AddSource, Remove, OnAction y SetProperty. Con Windows Installer versiones que se suministran con Windows Server 2003 y versiones posteriores, el [control SelectionTree](selectiontree-control.md) puede publicar la acción OnAction, ControlEvent, y SetProperty ControlEvents. El autor de la interfaz de usuario debe enumerar ControlEvent, en la [tabla ControlEvent,](controlevent-table.md). El controlador de la interfaz de usuario del instalador es el suscriptor a estos eventos.

[AddLocal ControlEvent,](addlocal-controlevent.md)

[AddSource ControlEvent,](addsource-controlevent.md)

[CheckExistingTargetPath ControlEvent,](checkexistingtargetpath-controlevent.md)

[CheckTargetPath ControlEvent,](checktargetpath-controlevent.md)

[ControlEvent, de acción](doaction-controlevent.md)

[EnableRollback ControlEvent,](enablerollback-controlevent.md)

[EndDialog ControlEvent,](enddialog-controlevent.md)

[NewDialog ControlEvent,](newdialog-controlevent.md)

[Reinstalar ControlEvent,](reinstall-controlevent.md)

[ReinstallMode ControlEvent,](reinstallmode-controlevent.md)

[Quitar ControlEvent,](remove-controlevent.md)

[Restablecer ControlEvent,](reset-controlevent.md)

[SetInstallLevel ControlEvent,](setinstalllevel-controlevent.md)

[SetProperty ControlEvent,](setproperty-controlevent.md)

[SetTargetPath ControlEvent,](settargetpath-controlevent.md)

[SpawnDialog ControlEvent,](spawndialog-controlevent.md)

[SpawnWaitDialog ControlEvent,](spawnwaitdialog-controlevent.md)

[ValidateProductID ControlEvent,](validateproductid-controlevent.md)

Un [control Pushbutton](pushbutton-control.md) puede publicar los eventos siguientes en un control [SelectionTree](selectiontree-control.md) de suscripción o en un [control DirectoryList](directorylist-control.md) ubicado en el mismo cuadro de diálogo. El control PushButton debe aparecer en la tabla ControlEvent, y los controles de suscripción deben aparecer en la tabla EventMapping.

[SelectionBrowse ControlEvent,](selectionbrowse-controlevent.md)

[DirectoryListUp ControlEvent,](directorylistup-controlevent.md)

[DirectoryListNew ControlEvent,](directorylistnew-controlevent.md)

[DirectoryListOpen ControlEvent,](directorylistopen-controlevent.md)

Normalmente, los eventos de control requieren que la interfaz de usuario se ejecute en el nivel de [*interfaz de usuario completo*](f-gly.md) . La mayoría de ControlEvents no funcionará con una interfaz de usuario [*básica*](b-gly.md) o una [*reducida*](r-gly.md) porque estos niveles solo muestran cuadros de diálogo no modales. Los eventos ActionText, AddSource, SetProgress, TimeRemaining y ScriptInProgress son excepciones y funcionarán en la interfaz de usuario básica o reducida. Para obtener más información sobre los niveles de interfaz de usuario, vea niveles de la [interfaz de usuario](user-interface-levels.md).

Puede ejecutar [acciones personalizadas](custom-actions.md) mediante la publicación de un ControlEvent, desde un [control Pushbutton](pushbutton-control.md) o un [control CheckBox](checkbox-control.md). Agregue un registro a la [tabla ControlEvent,](controlevent-table.md) con los nombres del cuadro de diálogo y el control que publica ControlEvent,. Este control debe publicar un [ControlEvent, de acción](doaction-controlevent.md) que notifique al instalador que ejecute la acción personalizada. En Windows XP o sistemas anteriores, no se puede ejecutar una acción personalizada mediante la publicación de un ControlEvent, desde un [control SelectionTree](selectiontree-control.md).

Para obtener más información sobre ControlEvents concretos, consulte la lista de [ControlEvents](control-events.md) estándar en [referencia](user-interface-reference.md)de la interfaz de usuario.

 

 
