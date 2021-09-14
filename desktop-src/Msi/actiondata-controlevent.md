---
description: El instalador usa este evento para publicar datos en la acción más reciente. Los datos se pueden mostrar en un cuadro de diálogo mediante un control de texto que se suscribe a este ControlEvent. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159235"
---
# <a name="actiondata-controlevent"></a>ActionData ControlEvent

El instalador usa este evento para publicar datos en la acción más reciente. Los datos se pueden mostrar en un cuadro de diálogo mediante un [control de texto](text-control.md) que se suscribe a este ControlEvent. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent se puede controlar mediante una [](r-gly.md)interfaz de usuario que se ejecuta en los niveles básico de interfaz de [*usuario,*](b-gly.md)interfaz de usuario reducida o interfaz [*de usuario*](f-gly.md) completa. Para obtener información sobre los niveles de interfaz de [usuario, vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Este control ControlEvent no usa ningún argumento.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Los suscriptores se ocultan cuando se inicia una nueva acción y se muestran cuando llegan nuevos datos de acción desde el instalador.

## <a name="typical-use"></a>Uso típico

Un [control de texto](text-control.md) en un cuadro de diálogo no modelo se suscribe a este evento a través de la tabla [EventMapping](eventmapping-table.md). El [atributo de control de](text-control-attribute.md) texto se muestra en el campo Atributos de esta tabla para recibir los datos de acción actuales. Normalmente se usa para mostrar los nombres de los archivos copiados durante la copia de archivos.

 

 



