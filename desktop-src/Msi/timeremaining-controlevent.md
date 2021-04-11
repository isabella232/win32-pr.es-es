---
description: El instalador usa el evento TimeRemaining para publicar el tiempo restante aproximado, en segundos, para la secuencia de progreso actual.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: TimeRemaining ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083302"
---
# <a name="timeremaining-controlevent"></a>TimeRemaining ControlEvent,

El instalador usa el evento TimeRemaining para publicar el tiempo restante aproximado, en segundos, para la secuencia de progreso actual. El tiempo restante se puede mostrar en un cuadro de diálogo mediante un [control de texto](text-control.md) que se suscribe a este ControlEvent,. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este ControlEvent, se puede controlar mediante una interfaz de usuario que se ejecuta en la interfaz de usuario [*básica*](b-gly.md), la interfaz de usuario [*reducida*](r-gly.md)o los niveles de [*IU completos*](f-gly.md) . Para obtener información sobre los niveles de interfaz de usuario, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un [control de texto](text-control.md) en un cuadro de diálogo no modal se suscribe a este evento a través de la [tabla EventMapping](eventmapping-table.md) y usa el [atributo TimeRemaining](timeremaining-control-attribute.md) para mostrar el tiempo restante.

El mismo control de texto que se suscribe a TimeRemaining ControlEvent, también puede suscribirse a [ScriptInProgress ControlEvent,](scriptinprogress-controlevent.md). En este caso, como la cadena de mensaje de ScriptInProgress preliminar, se reemplaza por la cadena "tiempo restante: XX minutos".

 

 



