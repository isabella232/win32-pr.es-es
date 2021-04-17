---
description: Este evento notifica al instalador, mientras mantiene el cuadro de diálogo presente en ejecución, que una característica o todas las características se van a ejecutar localmente.
ms.assetid: 074f347e-37d3-4365-a25d-caa0392a0dbc
title: AddLocal ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 112975d31e341c06a21609b173b9682283e71610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667053"
---
# <a name="addlocal-controlevent"></a>AddLocal ControlEvent,

Este evento notifica al instalador, mientras mantiene el cuadro de diálogo presente en ejecución, que una característica o todas las características se van a ejecutar localmente. Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md), un [control CheckBox](checkbox-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Una cadena, ya sea el nombre de la característica o "ALL".

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento y se utiliza para notificar al instalador sin detener el cuadro de diálogo.

 

 



