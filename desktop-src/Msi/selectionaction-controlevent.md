---
description: El control SelectionTree usa este evento para publicar una cadena que describe el elemento resaltado. La cadena es una de las &\# 0034; SEL \* & \# 0034; cadenas de la tabla UIText. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: SelectionAction ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669922"
---
# <a name="selectionaction-controlevent"></a>SelectionAction ControlEvent,

El [control SelectionTree](selectiontree-control.md) usa este evento para publicar una cadena que describe el elemento resaltado. La cadena es una de las cadenas "SEL \* " de la [tabla UIText](uitext-table.md). Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control de [texto](text-control.md) en el mismo cuadro de diálogo modal que el SelectionTree debería suscribirse a este evento a través de la [tabla EventMapping](eventmapping-table.md). El control de texto muestra la explicación del elemento seleccionado.

 

 



