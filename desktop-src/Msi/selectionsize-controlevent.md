---
description: El control SelectionTree usa el evento SelectionSize para publicar el tamaño del elemento resaltado.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: SelectionSize ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c8733c0155adc085343c0a5db1a42e3aa219719babb5b342781c5bb9923ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040365"
---
# <a name="selectionsize-controlevent"></a>SelectionSize ControlEvent

El [control SelectionTree](selectiontree-control.md) usa el evento SelectionSize para publicar el tamaño del elemento resaltado. Si es un elemento primario, también se publica el número de elementos secundarios seleccionados. La cadena es una de las cadenas **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos,** **SelParentCostPosNeg,** **SelParentCostNegPos** o **SelParentCostNegNeg de** la tabla [UIText](uitext-table.md). Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Control [Texto](text-control.md) en el mismo cuadro de diálogo modal que el control SelectionTree a través de [la tabla EventMapping](eventmapping-table.md). El Control de texto usa este evento para mostrar el tamaño del elemento resaltado.

 

 



