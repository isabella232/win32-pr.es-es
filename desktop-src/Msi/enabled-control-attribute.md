---
description: Este atributo especifica si el control especificado está habilitado o deshabilitado. La mayoría de los controles aparecen atenuados al deshabilitarlos.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Atributo de control habilitado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652532"
---
# <a name="enabled-control-attribute"></a>Atributo de control habilitado

Este atributo especifica si el control especificado está habilitado o deshabilitado. La mayoría de los controles aparecen atenuados al deshabilitarlos.

Si se establece este bit, el control se crea como habilitado.

Si no se establece este bit, el control se crea como deshabilitado.

## <a name="valid-controls"></a>Controles válidos

Todos los controles. La apariencia de algunos controles que no están asociados a una propiedad, como mapas de bits e iconos, no se ve afectada por el establecimiento de este atributo.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbControlAttributesEnabled** |



 

## <a name="remarks"></a>Observaciones

También puede usar la [tabla ControlCondition](controlcondition-table.md) para deshabilitar o habilitar un control según el valor de una propiedad o una instrucción condicional.

También puede habilitar o deshabilitar un control si suscribe el control a un [ControlEvent,](control-events.md). Escriba el identificador del atributo en la columna atributo y el identificador del evento en la columna evento de la [tabla EventMapping](eventmapping-table.md).

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



