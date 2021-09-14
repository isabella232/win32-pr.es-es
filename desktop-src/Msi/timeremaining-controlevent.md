---
description: El instalador usa el evento TimeRemaining para publicar el tiempo aproximado restante, en segundos, para la secuencia de progreso actual.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: TimeRemaining ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161434"
---
# <a name="timeremaining-controlevent"></a>TimeRemaining ControlEvent

El instalador usa el evento TimeRemaining para publicar el tiempo aproximado restante, en segundos, para la secuencia de progreso actual. El tiempo restante se puede mostrar en un cuadro de diálogo mediante un [control de texto](text-control.md) que se suscribe a este control ControlEvent. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent se puede controlar mediante una [](r-gly.md)interfaz de usuario que se ejecuta en los niveles de interfaz de usuario [*básica,*](b-gly.md)interfaz de usuario reducida o interfaz [*de usuario*](f-gly.md) completa. Para obtener información sobre los niveles de interfaz de [usuario, vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un [control De texto](text-control.md) en un cuadro de diálogo no modelo se suscribe a este evento a través de la tabla [EventMapping](eventmapping-table.md) y usa el atributo [TimeRemaining](timeremaining-control-attribute.md) para mostrar el tiempo restante.

El mismo control de texto que se suscribe a TimeRemaining ControlEvent también puede suscribirse a [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md). En este caso, como la cadena de mensaje ScriptInProgress preliminar, se reemplaza por la cadena "Tiempo restante: xx minutos".

 

 



