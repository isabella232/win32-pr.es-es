---
description: El control SelectionTree usa el evento SelectionBrowse para generar un cuadro de diálogo Examinar, lo que permite modificar la ruta de acceso del elemento resaltado.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: SelectionBrowse ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70d7c50e69921a5fefe7cff3c88c2351cacdecda42a164e8334c9afb3977bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040615"
---
# <a name="selectionbrowse-controlevent"></a>SelectionBrowse ControlEvent

El [control SelectionTree usa](selectiontree-control.md) el evento SelectionBrowse para generar un cuadro de diálogo Examinar, lo que permite modificar la ruta de acceso del elemento resaltado. 

Este evento debe publicarse mediante un [control PushButton ubicado](pushbutton-control.md) en el mismo cuadro de diálogo que el control que se suscribe a este evento. El evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

Los controles que publican un evento SelectionBrowse se deshabilitan si se ha seleccionado una característica que ya está instalada, no configurable o no seleccionada para la instalación local. Para poder configurarla, la característica debe tener una [propiedad pública](public-properties.md) especificada en el campo Directorio de la \_ tabla [Característica](feature-table.md).

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Nombre del cuadro de diálogo que se va a generar.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un [control PushButton](pushbutton-control.md) en el mismo cuadro de diálogo modal que SelectionTree usa este evento para desencadenar el **cuadro de** diálogo Examinar.

 

 



