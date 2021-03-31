---
description: El control SelectionTree usa el evento SelectionSize para publicar el tamaño del elemento resaltado.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: SelectionSize ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c11829661f0120fa5906a04f081e6c979b37180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277159"
---
# <a name="selectionsize-controlevent"></a>SelectionSize ControlEvent,

El [control SelectionTree](selectiontree-control.md) usa el evento SelectionSize para publicar el tamaño del elemento resaltado. Si es un elemento primario, también se publica el número de elementos secundarios seleccionados. La cadena es una de las cadenas **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** o **SelParentCostNegNeg** de la [tabla UIText](uitext-table.md). Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Control de [texto](text-control.md) en el mismo cuadro de diálogo modal que el control SelectionTree a través de la [tabla EventMapping](eventmapping-table.md). El control de texto utiliza este evento para mostrar el tamaño del elemento resaltado.

 

 



