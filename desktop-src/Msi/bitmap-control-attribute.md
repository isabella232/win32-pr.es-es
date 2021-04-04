---
description: Si se establece el bit de control Bitmap, el texto del control se sustituye por una imagen de mapa de bits. La columna de texto de la tabla de control es una clave externa de la tabla binaria.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Atributo de control Bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bda78231c1689c4c5faebeab98fbf6566c7e667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909054"
---
# <a name="bitmap-control-attribute"></a>Atributo de control Bitmap

Si se establece el bit de control Bitmap, el texto del control se sustituye por una imagen de mapa de bits. La columna de texto de la [tabla de control](control-table.md) es una clave externa de la [tabla binaria](binary-table.md).

Si no se establece este bit, el texto del control se especifica en la columna de texto de la [tabla de control](control-table.md).

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)

 

[Botones](pushbutton-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 262 144  | 0x00040000  | **msidbControlAttributesBitmap** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit de mapa de bits en la columna Attributes del registro del control en la [tabla de control](control-table.md).

La columna de texto de la tabla de control se usa como clave externa de la [tabla binaria](binary-table.md), por lo que el control no puede contener una imagen de icono y texto.

No establezca los bits de [icono](icon-control-attribute.md) y de mapa de bits.

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



