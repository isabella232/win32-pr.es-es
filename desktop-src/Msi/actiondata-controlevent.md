---
description: El instalador usa este evento para publicar datos sobre la acción más reciente. Los datos se pueden mostrar en un cuadro de diálogo mediante un control text que se suscribe a este control ControlEvent. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c280bbd2c0a184ec281e4401037687893942b4c344824b20a59c410b59fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105485"
---
# <a name="actiondata-controlevent"></a>ActionData ControlEvent

El instalador usa este evento para publicar datos sobre la acción más reciente. Los datos se pueden mostrar en un cuadro de diálogo mediante un [control text](text-control.md) que se suscribe a este control ControlEvent. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent se puede controlar mediante una [](r-gly.md)interfaz de usuario que se ejecuta en los niveles de interfaz de usuario [*básica,*](b-gly.md)interfaz de usuario reducida o interfaz [*de usuario*](f-gly.md) completa. Para obtener información sobre los niveles de interfaz de [usuario, vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Este control ControlEvent no usa un argumento.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Los suscriptores se ocultan cuando se inicia una nueva acción y se muestran cuando llegan nuevos datos de acción desde el instalador.

## <a name="typical-use"></a>Uso típico

Un [control De texto](text-control.md) en un cuadro de diálogo no modelo se suscribe a este evento a través de la tabla [EventMapping](eventmapping-table.md). El [atributo de control de](text-control-attribute.md) texto se muestra en el campo Atributos de esta tabla para recibir los datos de acción actuales. Normalmente se usa para mostrar los nombres de los archivos copiados durante la copia de archivos.

 

 



