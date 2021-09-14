---
description: Permite al autor especificar el modo o los modos de validación durante una reinstalación y mientras se ejecuta el cuadro de diálogo actual.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: ReinstallMode ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069669"
---
# <a name="reinstallmode-controlevent"></a>ReinstallMode ControlEvent

ReinstallMode ControlEventallows the author to specify the validation mode or modes during a reinstallation, and while the current dialog box is running.

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md) un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md)y requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funciona con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener más información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Una cadena. Para obtener una lista de los valores posibles, vea [**PROPIEDAD REINSTALLMODE.**](reinstallmode.md)

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Este evento está asociado a un control [PushButton](pushbutton-control.md) en un cuadro de diálogo modal. El mismo control [PushButton](pushbutton-control.md) también debe estar asociado a [un control Reinstall](reinstall-controlevent.md) ControlEvent.

 

 



