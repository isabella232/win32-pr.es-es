---
description: El control SelectionTree usa el evento SelectionPath para publicar la ruta de acceso del elemento resaltado.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45dfcb017c18b026f03bf9fa9b89d7be33db49bafc3dd9f899846cbada1047
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040445"
---
# <a name="selectionpath-controlevent"></a>SelectionPath ControlEvent

El [control SelectionTree](selectiontree-control.md) usa el evento SelectionPath para publicar la ruta de acceso del elemento resaltado. Si el elemento está seleccionado para ejecutarse desde el origen, esta es la ruta de acceso del origen. Si se selecciona que el elemento esté ausente, la cadena es la cadena **AbsentPath** de la [tabla UIText](uitext-table.md). Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un [control Text](text-control.md) en el mismo cuadro de diálogo modal que SelectionTree debe suscribirse al evento a través de la tabla [EventMapping](eventmapping-table.md). El Control de texto muestra la ruta de acceso del elemento resaltado.

 

 



