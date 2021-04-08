---
description: El instalador usa este evento para publicar el nombre de la acción actual. Un control de texto que se suscribe a este ControlEvent, puede mostrar el nombre en un cuadro de diálogo. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001765"
---
# <a name="actiontext-controlevent"></a>ActionText ControlEvent,

El instalador usa este evento para publicar el nombre de la acción actual. Un [control de texto](text-control.md) que se suscribe a este ControlEvent, puede mostrar el nombre en un cuadro de diálogo. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este ControlEvent, se puede controlar mediante una interfaz de usuario que se ejecuta en la interfaz de usuario [*básica*](b-gly.md), la interfaz de usuario [*reducida*](r-gly.md)o los niveles de [*IU completos*](f-gly.md) . Para obtener información sobre los niveles de interfaz de usuario, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Este ControlEvent, no utiliza un argumento.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Los suscriptores se muestran cuando llegan nuevos datos de progreso desde el instalador.

## <a name="typical-use"></a>Uso típico

Un [control de texto](text-control.md) en un cuadro de diálogo no modal se suscribe a este evento a través de la [tabla EventMapping](eventmapping-table.md). El [atributo control de texto](text-control-attribute.md) debe aparecer en el campo atributos de esta tabla para recibir el nombre de la acción actual.

 

 



