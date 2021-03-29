---
description: Permite al autor de especificar el modo de validación o los modos durante una reinstalación y mientras se está ejecutando el cuadro de diálogo actual.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: ReinstallMode ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652665"
---
# <a name="reinstallmode-controlevent"></a>ReinstallMode ControlEvent,

El ReinstallMode ControlEventallows el autor para especificar el modo de validación o los modos durante una reinstalación y mientras se está ejecutando el cuadro de diálogo actual.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md) o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md)y requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funciona con una interfaz de usuario [*básica*](b-gly.md)o no [*reducida*](r-gly.md) . Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Una cadena. Para obtener una lista de los valores posibles, vea [**REINSTALLMODE**](reinstallmode.md) (propiedad).

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Este evento está asociado a un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal. El mismo control [Pushbutton](pushbutton-control.md) también debe estar vinculado a un ControlEvent, de [reinstalación](reinstall-controlevent.md) .

 

 



