---
description: Este evento notifica al instalador que se va a pasar un cuadro de diálogo modal a otro cuadro de diálogo. El instalador quita el cuadro de diálogo presente y crea el nuevo con el nombre indicado en el argumento.
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: NewDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155520"
---
# <a name="newdialog-controlevent"></a>NewDialog ControlEvent,

Este evento notifica al instalador que se va a pasar un cuadro de diálogo modal a otro cuadro de diálogo. El instalador quita el cuadro de diálogo presente y crea el nuevo con el nombre indicado en el argumento.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Cadena que es el nombre del nuevo cuadro de diálogo.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo modal está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para indicar una transición al cuadro de diálogo siguiente o anterior de la misma secuencia del asistente.

 

 



