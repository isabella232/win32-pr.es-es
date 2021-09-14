---
description: Si se establece el bit De control FixedSize, la imagen se recorta o se centra en el control sin cambiar su forma o tamaño.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Atributo de control FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074773"
---
# <a name="fixedsize-control-attribute"></a>Atributo de control FixedSize

Si se establece el bit De control FixedSize, la imagen se recorta o se centra en el control sin cambiar su forma o tamaño.

Si no se establece este bit, la imagen se ajusta para ajustarse al control.

## <a name="valid-controls"></a>Controles válidos

[Bitmap](bitmap-control.md)

[CheckBox](checkbox-control.md)

[Icono](icon-control.md)

[Pulsador](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                            |
|---------|-------------|-------------------------------------|
| 1 048 576 | 0x00100000  | **msidbControlAttributesFixedSize** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control , incluya el bit FixedSize en la columna Attributes del registro del control en la [tabla Control](control-table.md).

Establecer el bit FixedSize no tiene ningún efecto [](icon-control-attribute.md) en [checkBox,](checkbox-control.md) [](bitmap-control-attribute.md) [PushButton](pushbutton-control.md)o [RadioButtonGroup](radiobuttongroup-control.md) si no se han establecido ni el mapa de bits ni el icono.

Establecer el bit FixedSize no tiene ningún efecto en un control Icon ni en un PushButton asociado a un icono, si no se establecen los bits [IconSize.](iconsize-control-attribute.md)

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



