---
description: Si se establece el bit de control visible, el control está visible en el cuadro de diálogo. Si no se establece este bit, el control se oculta en el cuadro de diálogo. Un evento de control puede cambiar posteriormente el estado oculto o visible del atributo de control visible.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Atributo de control visible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677351"
---
# <a name="visible-control-attribute"></a>Atributo de control visible

Si se establece el bit de control visible, el control está visible en el cuadro de diálogo. Si no se establece este bit, el control se oculta en el cuadro de diálogo. Un [evento de control](control-events.md)puede cambiar posteriormente el estado oculto o visible del atributo de control visible.

## <a name="valid-controls"></a>Controles válidos

Todos los controles.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 1       | 0x00000001  | **msidbControlAttributesVisible** |



 

## <a name="remarks"></a>Observaciones

Puede usar la [tabla ControlCondition](controlcondition-table.md) para mostrar u ocultar un control según el valor de una propiedad o una instrucción condicional. También puede mostrar u ocultar un control si suscribe el control a un [ControlEvent,](control-events.md). Escriba el identificador del atributo en la columna atributo y el identificador del evento en la columna evento de la [tabla EventMapping](eventmapping-table.md).

Vea [controles y](controls.md) [atributos de control](control-attributes.md) .

 

 



