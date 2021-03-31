---
description: La tabla TextStyle muestra los distintos estilos de fuente que se usan en los controles que tienen texto.
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: Tabla de TextStyle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001286"
---
# <a name="textstyle-table"></a>Tabla de TextStyle

La tabla TextStyle muestra los distintos estilos de fuente que se usan en los controles que tienen texto.

La tabla TextStyle tiene las columnas siguientes.



| Columna    | Tipo                               | Clave | Nullable |
|-----------|------------------------------------|-----|----------|
| Estilo] | [Identificador](identifier.md)       | Y   | N        |
| FaceName  | [Texto](text.md)                   | N   | N        |
| Tamaño      | [Entero](integer.md)             | N   | N        |
| Color     | [DoubleInteger](doubleinteger.md) | N   | Y        |
| StyleBits | [Entero](integer.md)             | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>Estilo]
</dt> <dd>

Esta columna es el nombre del estilo de fuente. Este nombre se puede incrustar en la cadena de texto para indicar un cambio de estilo. Tenga en cuenta que el nombre de estilo de fuente utilizado en este campo no debe acabar con los caracteres: \_ UL. Vea [Agregar controles y texto](adding-controls-and-text.md).

</dd> <dt>

<span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName
</dt> <dd>

Cadena que indica el nombre de la fuente. La cadena no debe tener más de 31 caracteres de longitud.

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>Ajusta
</dt> <dd>

Tamaño de fuente medido en puntos. Debe ser un número no negativo.

</dd> <dt>

<span id="Color"></span><span id="color"></span><span id="COLOR"></span>Color
</dt> <dd>

Esta columna especifica el color del texto que se muestra en un [control de texto](text-control.md). Todos los demás tipos de controles siempre utilizan el color de texto predeterminado. El valor colocado en esta columna debe calcularse mediante la siguiente fórmula: 65536 \* azul + 256 \* verde + rojo, donde rojo, verde y azul están cada uno en el intervalo de 0-255. El valor no debe superar 16777215, que es el valor de blanco. El valor es 0 para negro, 255 para rojo, 65280 para verde, 16711680 para azul y 8421504 para gris. Al dejar el campo vacío, se especifica el color predeterminado.

No coloque controles de [texto](text-control.md) transparente sobre los mapas de bits de color. Es posible que el texto no esté visible si el usuario cambia la combinación de colores de la pantalla. Por ejemplo, el texto puede volverse invisible si el usuario establece el parámetro de contraste alto para accesibilidad.

</dd> <dt>

<span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits
</dt> <dd>

Combinación de bits que indica el formato del texto.

Los bits de estilo individuales tienen los siguientes valores.



| Constante                             | Hexadecimal | Decimal | Estilo      |
|--------------------------------------|-------------|---------|------------|
| **msidbTextStyleStyleBitsBold**      | 0x001       | 1       | Bold       |
| **msidbTextStyleStyleBitsItalic**    | 0x002       | 2       | Cursiva     |
| **msidbTextStyleStyleBitsUnderline** | 0x004       | 4       | Subrayado  |
| **msidbTextStyleStyleBitsStrike**    | 0x008       | 8       | Golpear |



 

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE31](ice31.md)  
[ICE45](ice45.md)  
</dl>

 

 



