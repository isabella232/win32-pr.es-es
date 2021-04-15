---
description: El control SelectionTree usa el evento SelectionPathOn para publicar un valor booleano que indica si hay una ruta de acceso de selección asociada a la característica seleccionada actualmente. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669921"
---
# <a name="selectionpathon-controlevent"></a>SelectionPathOn ControlEvent,

El [control SelectionTree](selectiontree-control.md) usa el evento SelectionPathOn para publicar un valor booleano que indica si hay una ruta de acceso de selección asociada a la característica seleccionada actualmente. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

La SelectionPathOn ControlEvent, no se publica nunca durante una [instalación de mantenimiento](maintenance-installation.md).

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control de [texto](text-control.md) en el mismo cuadro de diálogo modal que el SelectionTree debe suscribirse al evento a través de la [tabla EventMapping](eventmapping-table.md). El control de texto muestra el título de la ruta de acceso de la selección. Este control de texto está visible u oculto dependiendo del evento.

 

 



