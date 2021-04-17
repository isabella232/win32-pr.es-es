---
description: El control SelectionTree usa el evento SelectionNoItems para eliminar el texto de Descripción del elemento obsoleto o para deshabilitar los botones que han dejado de ser útiles. Este evento debe crearse en la tabla EventMapping.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653081"
---
# <a name="selectionnoitems-controlevent"></a>SelectionNoItems ControlEvent,

El [control SelectionTree](selectiontree-control.md) usa el evento SelectionNoItems para eliminar el texto de Descripción del elemento obsoleto o para deshabilitar los botones que han dejado de ser útiles. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) . Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida. Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

Este evento solo puede afectar a los controles que se encuentran en el mismo cuadro de diálogo que el control SelectionTree.

## <a name="published-by"></a>Publicado por

[Control SelectionTree](selectiontree-control.md) si la selección no tiene ningún nodo.

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Elimina el texto de Descripción del elemento obsoleto o deshabilita los botones obsoletos.

## <a name="typical-use"></a>Uso típico

Se puede usar para deshabilitar los botones siguiente, restablecer y DiskCost en el [cuadro de diálogo de selección](selection-dialog.md) cuando una selección no tiene ningún nodo y estos botones pasan a ser inservibles.

 

 



