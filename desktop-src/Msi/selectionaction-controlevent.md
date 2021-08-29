---
description: El control SelectionTree usa este evento para publicar una cadena que describe el elemento resaltado. La cadena es una de las &\# 0034; Sel \* & \# 0034; cadenas de la tabla UIText. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: SelectionAction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2353c967eb6a7a0160a647b51ac0eff87ad187499147f3c051bc8eb33086df88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040655"
---
# <a name="selectionaction-controlevent"></a>SelectionAction ControlEvent

El [control SelectionTree](selectiontree-control.md) usa este evento para publicar una cadena que describe el elemento resaltado. La cadena es una de las \* cadenas "Sel" de la tabla [UIText](uitext-table.md). Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un [control Text](text-control.md) en el mismo cuadro de diálogo modal que SelectionTree debe suscribirse a este evento a través de la tabla [EventMapping](eventmapping-table.md). El Control de texto muestra la explicación del elemento seleccionado.

 

 



