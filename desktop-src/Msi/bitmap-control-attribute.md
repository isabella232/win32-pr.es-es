---
description: Si se establece el bit Control de mapa de bits, el texto del control se reemplaza por una imagen de mapa de bits. La columna Text de la tabla Control es una clave externa en la tabla Binary.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Atributo de control de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2cd7ea8186d1ed16de71ae9974bb67a082142ed3e921d023ad905d4f47bbc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638744"
---
# <a name="bitmap-control-attribute"></a>Atributo de control de mapa de bits

Si se establece el bit Control de mapa de bits, el texto del control se reemplaza por una imagen de mapa de bits. La columna Text de la [tabla Control es](control-table.md) una clave externa en la tabla [Binaria.](binary-table.md)

Si no se establece este bit, el texto del control se especifica en la columna Texto de la [tabla Control](control-table.md).

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)

 

[Pulsador](pushbutton-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 262 144  | 0x00040000  | **msidbControlAttributesBitmap** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control , incluya el bit Bitmap en la columna Atributos del registro del control en la [tabla Control](control-table.md).

La columna Text de la tabla Control se usa como clave externa para la tabla [Binary,](binary-table.md)por lo que el control no puede contener una imagen de icono y texto.

No establezca los bits [Icono y](icon-control-attribute.md) Mapa de bits.

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



