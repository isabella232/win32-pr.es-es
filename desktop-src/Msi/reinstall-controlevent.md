---
description: Permite al autor iniciar una reinstalación de algunas o todas las características, mientras el cuadro de diálogo actual se está ejecutando.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: Reinstalar ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667150"
---
# <a name="reinstall-controlevent"></a>Reinstalar ControlEvent,

La reinstalación ControlEventallows el autor para iniciar una reinstalación de algunas o todas las características, mientras se ejecuta el cuadro de diálogo actual.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md) o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md)y requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funciona con una interfaz de usuario [*básica*](b-gly.md)o no [*reducida*](r-gly.md) . Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Cadena que es el nombre de la característica o "ALL".

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Este evento está asociado a un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal. El mismo control [Pushbutton](pushbutton-control.md) también debe estar vinculado a un [ReinstallMode](reinstallmode-controlevent.md) ControlEvent,.

 

 



