---
description: El control SelectionTree usa el evento SelectionPath para publicar la ruta de acceso del elemento resaltado.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002139"
---
# <a name="selectionpath-controlevent"></a>SelectionPath ControlEvent,

El [control SelectionTree](selectiontree-control.md) usa el evento SelectionPath para publicar la ruta de acceso del elemento resaltado. Si el elemento está seleccionado para ejecutarse desde el origen, se trata de la ruta de acceso del origen. Si el elemento está seleccionado para estar ausente, la cadena es la cadena **AbsentPath** de la [tabla UIText](uitext-table.md). Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.

## <a name="published-by"></a>Publicado por

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control de [texto](text-control.md) en el mismo cuadro de diálogo modal que el SelectionTree debe suscribirse al evento a través de la [tabla EventMapping](eventmapping-table.md). El control de texto muestra la ruta de acceso del elemento resaltado.

 

 



