---
description: Un archivo de icono puede contener varios tamaños diferentes de la misma imagen de icono.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: IconSize (atributo de control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7323d9c3d8dc9bef1bfd4cd275a20dfcadaa3be946bc78fd358a2d6484db53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894205"
---
# <a name="iconsize-control-attribute"></a>IconSize (atributo de control)

Un archivo de icono puede contener varios tamaños diferentes de la misma imagen de icono. Estos bits especifican el tamaño de la imagen de icono que se va a cargar. Si no se establece ninguno de los bits, se carga la primera imagen. Si solo **se establece msidbControlAttributesIconSize16,** se carga la primera imagen de 16 x 16. Si solo se **establece msidbControlAttributesIconSize32,** se carga la primera imagen de 32x32. Si **se establece msidbControlAttributesIconSize48,** se carga la primera imagen de 48x48.

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)

[Icono](icon-control.md)

[Pulsador](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Descripción                          |
|---------|-------------|--------------------------------------|
| 2 097 152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| 4 194 304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control , incluya los bits IconSize en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Si no se establece el bit [FixedSize,](fixedsize-control-attribute.md) la imagen cargada se reducirá o se ajustará para ajustarse al control de icono. Si se establece el bit [FixedSize](fixedsize-control-attribute.md) y la imagen cargada es menor que el control de icono, la imagen se muestra centrada dentro del control. Si se establece el bit [FixedSize](fixedsize-control-attribute.md) y la imagen cargada es mayor que el control de icono, la imagen se reduce para ajustarse al control.

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



