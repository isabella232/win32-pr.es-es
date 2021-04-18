---
description: Este evento notifica al instalador que tiene que comprobar que se puede escribir en la ruta de acceso seleccionada. Si no se puede escribir la ruta de acceso, el evento bloquea más ControlEvents asociadas al control.
ms.assetid: 4672e2e4-a789-4050-81b9-92ec491745ac
title: CheckExistingTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1117de57c5474d196da1f40da6fda3cce60b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652592"
---
# <a name="checkexistingtargetpath-controlevent"></a>CheckExistingTargetPath ControlEvent,

Este evento notifica al instalador que tiene que comprobar que se puede escribir en la ruta de acceso seleccionada. Si no se puede escribir la ruta de acceso, el evento bloquea más ControlEvents asociadas al control.

Este evento puede ser publicado por un [control Pushbutton](pushbutton-control.md)o un [control SelectionTree](selectiontree-control.md). Este evento se debe crear en la [tabla ControlEvent,](controlevent-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Nombre de la propiedad que contiene la ruta de acceso. Si la propiedad está indirecta, el nombre de la propiedad se incluye entre corchetes.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Este ControlEvent, no realiza ninguna acción en los suscriptores.

## <a name="typical-use"></a>Uso típico

Un control [Pushbutton](pushbutton-control.md) en un cuadro de diálogo de exploración está asociado a este evento en la tabla [ControlEvent,](controlevent-table.md) para comprobar la ruta de acceso seleccionada antes de volver al cuadro de diálogo de selección.

 

 



