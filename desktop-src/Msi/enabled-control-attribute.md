---
description: Este atributo especifica si el control especificado está habilitado o deshabilitado. La mayoría de los controles aparecen en gris cuando están deshabilitados.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Atributo de control habilitado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158494"
---
# <a name="enabled-control-attribute"></a>Atributo de control habilitado

Este atributo especifica si el control especificado está habilitado o deshabilitado. La mayoría de los controles aparecen en gris cuando están deshabilitados.

Si se establece este bit, el control se crea como habilitado.

Si no se establece este bit, el control se crea como deshabilitado.

## <a name="valid-controls"></a>Controles válidos

Todos los controles. La apariencia de algunos controles que no están asociados a una propiedad, como mapas de bits e iconos, no se ven afectados al establecer este atributo.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 2       | 0x00000002  | **msidbControlAttributesEnabled** |



 

## <a name="remarks"></a>Observaciones

También puede usar la [tabla ControlCondition para](controlcondition-table.md) deshabilitar o habilitar un control según el valor de una propiedad o instrucción condicional.

También puede habilitar o deshabilitar un control suscribiendo el control a [un control ControlEvent](control-events.md). Escriba el identificador del atributo en la columna Atributo y el identificador del evento en la columna Evento de la [tabla EventMapping](eventmapping-table.md).

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



