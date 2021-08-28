---
description: Si se establece el bit De control FixedSize, la imagen se recorta o se centra en el control sin cambiar su forma o tamaño.
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: Atributo de control FixedSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40094001115dc6e196e66075abe7ace7c93c8e715818ad34235f80caf8306a06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649705"
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

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                            |
|---------|-------------|-------------------------------------|
| 1 048 576 | 0x00100000  | **msidbControlAttributesFixedSize** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control, incluya el bit FixedSize en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Establecer el bit FixedSize no tiene ningún efecto [](icon-control-attribute.md) en [checkBox,](checkbox-control.md) [](bitmap-control-attribute.md) [PushButton](pushbutton-control.md)o [RadioButtonGroup](radiobuttongroup-control.md) si no se han establecido ni el mapa de bits ni el icono.

Establecer el bit FixedSize no tiene ningún efecto en un control Icon ni en un PushButton asociado a un icono, si no se establecen los bits [IconSize.](iconsize-control-attribute.md)

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



