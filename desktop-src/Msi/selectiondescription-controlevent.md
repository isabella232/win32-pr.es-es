---
description: El control SelectionTree usa el evento SelectionDescription para publicar una cadena que contiene la descripción del elemento resaltado. Esta cadena es el campo Descripción de la tabla Característica. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: SelectionDescription ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac1d7a6fdfa4e215e0f659b5f3341404e2376f5e82f3c1d019a35e833995e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040585"
---
# <a name="selectiondescription-controlevent"></a>SelectionDescription ControlEvent

El [control SelectionTree](selectiontree-control.md) usa el evento SelectionDescription para publicar una cadena que contiene la descripción del elemento resaltado. Esta cadena es el **campo Description** de la [tabla Feature](feature-table.md). Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el [control SelectionTree](selectiontree-control.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener más información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un [control Text](text-control.md) en el mismo cuadro de diálogo modal que SelectionTree se suscribe a este controlEvent a través de la tabla [EventMapping](eventmapping-table.md). El control Text usa este evento para mostrar la descripción del elemento resaltado.

 

 



