---
description: Si se establece el bit Control visible, el control está visible en el cuadro de diálogo. Si no se establece este bit, el control se oculta en el cuadro de diálogo. Un evento de control puede cambiar más adelante el estado visible u oculto del atributo de control Visible.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Atributo de control visible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abdecdc46f179b7639a6ecaa627d92b643ed781ade242a152262d38c46f7eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498805"
---
# <a name="visible-control-attribute"></a>Atributo de control visible

Si se establece el bit Control visible, el control está visible en el cuadro de diálogo. Si no se establece este bit, el control se oculta en el cuadro de diálogo. Un evento de control puede cambiar más adelante el estado visible u oculto del [atributo de control Visible.](control-events.md)

## <a name="valid-controls"></a>Controles válidos

Todos los controles.

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 1       | 0x00000001  | **msidbControlAttributesVisible** |



 

## <a name="remarks"></a>Comentarios

Puede usar la [tabla ControlCondition para](controlcondition-table.md) mostrar u ocultar un control según el valor de una propiedad o instrucción condicional. También puede mostrar u ocultar un control suscribiendo el control a [un control ControlEvent](control-events.md). Escriba el identificador del atributo en la columna Atributo y el identificador del evento en la columna Evento de la [tabla EventMapping](eventmapping-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



