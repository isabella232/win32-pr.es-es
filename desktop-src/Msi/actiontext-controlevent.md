---
description: El instalador usa este evento para publicar el nombre de la acción actual. El nombre se puede mostrar en un cuadro de diálogo mediante un control de texto que se suscribe a este ControlEvent. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159229"
---
# <a name="actiontext-controlevent"></a>ActionText ControlEvent

El instalador usa este evento para publicar el nombre de la acción actual. El nombre se puede mostrar en un cuadro de diálogo mediante un [control de texto](text-control.md) que se suscribe a este ControlEvent. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent se puede controlar mediante una [](r-gly.md)interfaz de usuario que se ejecuta en los niveles básico de interfaz de [*usuario,*](b-gly.md)interfaz de usuario reducida o interfaz [*de usuario*](f-gly.md) completa. Para obtener información sobre los niveles de interfaz de usuario, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Este control ControlEvent no usa ningún argumento.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Los suscriptores se muestran cuando llegan nuevos datos de progreso desde el instalador.

## <a name="typical-use"></a>Uso típico

Un [control De texto](text-control.md) en un cuadro de diálogo no modelo se suscribe a este evento a través de la tabla [EventMapping](eventmapping-table.md). El [atributo de control de](text-control-attribute.md) texto debe aparecer en el campo Atributos de esta tabla para recibir el nombre de la acción actual.

 

 



