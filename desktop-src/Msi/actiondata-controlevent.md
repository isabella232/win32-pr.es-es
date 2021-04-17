---
description: El instalador usa este evento para publicar datos en la acción más reciente. Los datos se pueden mostrar en un cuadro de diálogo mediante un control de texto que se suscribe a este ControlEvent,. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667061"
---
# <a name="actiondata-controlevent"></a>ActionData ControlEvent,

El instalador usa este evento para publicar datos en la acción más reciente. Los datos se pueden mostrar en un cuadro de diálogo mediante un [control de texto](text-control.md) que se suscribe a este ControlEvent,. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este ControlEvent, se puede controlar mediante una interfaz de usuario que se ejecuta en la interfaz de usuario [*básica*](b-gly.md), la interfaz de usuario [*reducida*](r-gly.md)o los niveles de [*IU completos*](f-gly.md) . Para obtener información sobre los niveles de interfaz de usuario, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Este ControlEvent, no utiliza un argumento.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Los suscriptores se ocultan cuando se inicia una nueva acción y se muestran cuando llegan nuevos datos de acción desde el instalador.

## <a name="typical-use"></a>Uso típico

Un [control de texto](text-control.md) en un cuadro de diálogo no modal se suscribe a este evento a través de la [tabla EventMapping](eventmapping-table.md). El [atributo control de texto](text-control-attribute.md) se muestra en el campo atributos de esta tabla para recibir los datos de la acción actual. Normalmente se usa para mostrar los nombres de los archivos copiados durante la copia de archivos.

 

 



