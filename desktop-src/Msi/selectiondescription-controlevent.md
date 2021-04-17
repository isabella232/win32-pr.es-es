---
description: El control SelectionTree usa el evento SelectionDescription para publicar una cadena que contiene la descripción del elemento resaltado. Esta cadena es el campo de descripción de la tabla de características. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: SelectionDescription ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667619"
---
# <a name="selectiondescription-controlevent"></a>SelectionDescription ControlEvent,

El [control SelectionTree](selectiontree-control.md) usa el evento SelectionDescription para publicar una cadena que contiene la descripción del elemento resaltado. Esta cadena es el campo de **Descripción** de la [tabla de características](feature-table.md). Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el [control SelectionTree](selectiontree-control.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control de [texto](text-control.md) en el mismo cuadro de diálogo modal que el SelectionTree se suscribe a este ControlEvent, a través de la [tabla EventMapping](eventmapping-table.md). El control de texto utiliza este evento para mostrar la descripción del elemento resaltado.

 

 



