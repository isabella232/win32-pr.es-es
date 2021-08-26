---
description: El control SelectionTree usa el evento SelectionPathOn para publicar un valor booleano que indica si hay una ruta de acceso de selección asociada a la característica seleccionada actualmente. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea32926117c200f466bd2c40ac611e7ccbc47fb6a231a5dcf93ffa2ee0446b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040435"
---
# <a name="selectionpathon-controlevent"></a>SelectionPathOn ControlEvent

El [control SelectionTree usa](selectiontree-control.md) el evento SelectionPathOn para publicar un valor booleano que indica si hay una ruta de acceso de selección asociada a la característica seleccionada actualmente. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

SelectionPathOn ControlEvent nunca se publica durante una instalación [de mantenimiento.](maintenance-installation.md)

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un [control Text](text-control.md) en el mismo cuadro de diálogo modal que SelectionTree debe suscribirse al evento a través de la tabla [EventMapping](eventmapping-table.md). El Control de texto muestra el título de la ruta de acceso de selección. Este control de texto está visible u oculto en función del evento.

 

 



