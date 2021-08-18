---
description: El control SelectionTree usa el evento SelectionNoItems para eliminar el texto de descripción del elemento obsoleto o para deshabilitar los botones que se han vuelto inutilizados. Este evento debe crearse en la tabla EventMapping.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17220849c6bf50a28a0a0596bcd347e2f0a4c5af77cb53c9d9fa0041ced59abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040465"
---
# <a name="selectionnoitems-controlevent"></a>SelectionNoItems ControlEvent

El [control SelectionTree usa](selectiontree-control.md) el evento SelectionNoItems para eliminar el texto de descripción del elemento obsoleto o para deshabilitar los botones que se han vuelto inutilizados. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.

## <a name="published-by"></a>Publicado por

[Control SelectionTree](selectiontree-control.md) si la selección no tiene nodos.

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Elimina el texto de descripción del elemento obsoleto o deshabilita los botones obsoletos.

## <a name="typical-use"></a>Uso típico

Se puede usar para deshabilitar los botones Siguiente, Restablecer y DiskCost en el cuadro de diálogo Selección cuando una selección no tiene nodos y estos botones se vuelven inservibles. [](selection-dialog.md)

 

 



