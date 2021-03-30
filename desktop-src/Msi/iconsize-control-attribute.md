---
description: Un archivo de icono puede contener varios tamaños diferentes de la misma imagen de icono.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Atributo de control de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082535"
---
# <a name="iconsize-control-attribute"></a>Atributo de control de iconos

Un archivo de icono puede contener varios tamaños diferentes de la misma imagen de icono. Estos bits especifican el tamaño de la imagen del icono que se va a cargar. Si no se establece ninguno de los bits, se carga la primera imagen. Si solo se establece **msidbControlAttributesIconSize16** , se carga la primera imagen 16x16. Si solo se establece **msidbControlAttributesIconSize32** , se carga la primera imagen de 32x32. Si se establece **msidbControlAttributesIconSize48** , se carga la primera imagen 48x48.

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)

[Icono](icon-control.md)

[Botones](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Descripción                          |
|---------|-------------|--------------------------------------|
| 2 097 152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| 4 194 304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya los bits de los iconos en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Si no se establece el bit [FixedSize](fixedsize-control-attribute.md) , la imagen cargada se reduce o se ajusta para ajustarse al control de icono. Si se establece el bit [FixedSize](fixedsize-control-attribute.md) y la imagen cargada es más pequeña que el control de icono, la imagen se muestra centrada dentro del control. Si se establece el bit [FixedSize](fixedsize-control-attribute.md) y la imagen cargada es mayor que el control de icono, la imagen se reduce para ajustarse al control.

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



