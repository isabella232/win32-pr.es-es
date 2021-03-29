---
description: Si se establece el bit de control FixedSize, la imagen se recorta o se centra en el control sin cambiar su forma o tamaño.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Atributo de control FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809506"
---
# <a name="fixedsize-control-attribute"></a>Atributo de control FixedSize

Si se establece el bit de control FixedSize, la imagen se recorta o se centra en el control sin cambiar su forma o tamaño.

Si no se establece este bit, la imagen se ajusta para ajustarse al control.

## <a name="valid-controls"></a>Controles válidos

[Bitmap](bitmap-control.md)

[CheckBox](checkbox-control.md)

[Icono](icon-control.md)

[Botones](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                            |
|---------|-------------|-------------------------------------|
| 1 048 576 | 0x00100000  | **msidbControlAttributesFixedSize** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit FixedSize en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Establecer el bit FixedSize no tiene ningún efecto en [CheckBox](checkbox-control.md), [Pushbutton](pushbutton-control.md)o [RadioButtonGroup](radiobuttongroup-control.md) si no se ha establecido el [mapa](bitmap-control-attribute.md) de bits o el [icono](icon-control-attribute.md) .

Establecer el bit FixedSize no tiene ningún efecto en un control de icono o un botón de opción asociado a un icono si no se establece el valor de los [iconos](iconsize-control-attribute.md) de los bits.

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



