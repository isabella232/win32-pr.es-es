---
description: El control ControlEvent de DoAction notifica al instalador que ejecute una acción personalizada. Este evento se puede publicar mediante un control PushButton, un control CheckBox o un control SelectionTree. Este evento debe crearse en la tabla ControlEvent.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: DoAction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158522"
---
# <a name="doaction-controlevent"></a>DoAction ControlEvent

El control ControlEvent de DoAction notifica al instalador que ejecute una acción personalizada. Este evento se puede publicar mediante un control [PushButton,](pushbutton-control.md) un control [CheckBox](checkbox-control.md) o un control [SelectionTree.](selectiontree-control.md) Este evento debe crearse en la [tabla ControlEvent.](controlevent-table.md)

Tenga en cuenta que las acciones personalizadas iniciadas por un control ControlEvent de DoAction pueden enviar un mensaje con el método [**Message**](session-message.md), pero no puede enviar un mensaje [**con MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). En sistemas anteriores a Windows Server 2003, las acciones personalizadas iniciadas por un control DoAction ControlEvent no pueden enviar mensajes con **MsiProcessMessage** o **message Method**. Para obtener más información, vea [Enviar mensajes a Windows instalador mediante MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener más información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Cadena, el nombre de la acción personalizada que se va a ejecutar.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Este control ControlEvent no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un [control PushButton](pushbutton-control.md) de un cuadro de diálogo está vinculado a este evento en la [tabla ControlEvent](controlevent-table.md) para invocar una acción personalizada.

 

 



