---
description: La ControlEvent, de la acción notifica al instalador que ejecute una acción personalizada. Este evento puede ser publicado por un control PushButton, un control CheckBox o un control SelectionTree. Este evento se debe crear en la tabla ControlEvent,.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: ControlEvent, de acción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153881"
---
# <a name="doaction-controlevent"></a>ControlEvent, de acción

La ControlEvent, de la acción notifica al instalador que ejecute una acción personalizada. Este evento puede ser publicado por un control [Pushbutton](pushbutton-control.md) , un control [CheckBox](checkbox-control.md) o un control [SelectionTree](selectiontree-control.md) . Este evento se debe crear en la tabla [ControlEvent,](controlevent-table.md) .

Tenga en cuenta que las acciones personalizadas iniciadas por un ControlEvent, de acción pueden enviar un mensaje con el [**método de mensaje**](session-message.md), pero no puede enviar un mensaje con [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). En sistemas anteriores a Windows Server 2003, las acciones personalizadas iniciadas por una acción ControlEvent, no pueden enviar mensajes con **MsiProcessMessage** o un **método de mensaje**. Para obtener más información, consulte [envío de mensajes a Windows Installer mediante MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Una cadena, el nombre de la acción personalizada que se va a ejecutar.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para invocar una acción personalizada.

 

 



