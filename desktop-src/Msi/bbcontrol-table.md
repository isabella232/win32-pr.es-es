---
description: En la tabla BBControl se enumeran los controles que se mostrarán en cada uno de ellos.
ms.assetid: 2ab31a32-6d33-46b7-a295-199560efa7fb
title: Tabla BBControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70198167c866195204ec6cbcf644b92f3489a4ff44e14e719efbf5c6647e30c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754375"
---
# <a name="bbcontrol-table"></a>Tabla BBControl

En la tabla BBControl se enumeran los controles que se mostrarán en cada uno de ellos.

La tabla BBControl tiene las columnas siguientes.



| Columna      | Tipo                               | Clave | Nullable |
|-------------|------------------------------------|-----|----------|
| Cartelera\_ | [Identificador](identifier.md)       | Y   | N        |
| BBControl   | [Identificador](identifier.md)       | Y   | N        |
| Tipo        | [Identificador](identifier.md)       | N   | N        |
| X           | [Entero](integer.md)             | N   | N        |
| Y           | [Entero](integer.md)             | N   | N        |
| Ancho       | [Entero](integer.md)             | N   | N        |
| Alto      | [Entero](integer.md)             | N   | N        |
| Atributos  | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Texto        | [Texto](text.md)                   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Billboard_"></span><span id="billboard_"></span><span id="BILLBOARD_"></span>Cartelera\_
</dt> <dd>

Nombre del cuadro.

Clave externa para la columna uno de la [tabla DeÓnón](billboard-table.md).

</dd> <dt>

<span id="BBControl"></span><span id="bbcontrol"></span><span id="BBCONTROL"></span>BBControl
</dt> <dd>

Nombre del control. Este nombre debe ser único dentro de un cuadro, pero se puede repetir en diferentes estaciones. Esta columna combinada con la columna Column \_ forma la clave principal de la tabla.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Tipo del control. Solo se pueden colocar controles estáticos, [como texto,](text-control.md) [mapa de bits,](bitmap-control.md) [icono](icon-control.md)o control personalizado en un lápiz. Para obtener una lista completa de los controles, vea la [sección Controles.](controls.md)

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Coordenada horizontal de la esquina superior izquierda del límite rectangular del control. Las unidades son [unidades del instalador.](installer-units.md) Esta coordenada se mide en relación con el control de la marca y no con respecto al cuadro de diálogo. Use solo números no negativos.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Coordenada vertical de la esquina superior izquierda del límite rectangular del control. Las unidades son [unidades del instalador.](installer-units.md) Esta coordenada se mide en relación con el control de la marca y no con respecto al cuadro de diálogo. Este número no debe ser negativo.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Ancho
</dt> <dd>

Ancho del límite rectangular del control. Las unidades son [unidades del instalador.](installer-units.md) Este número no debe ser negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Altura
</dt> <dd>

Alto del límite rectangular del control. Las unidades son [unidades del instalador.](installer-units.md) Este número no debe ser negativo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Palabra de 32 bits que especifica las marcas de atributo que se aplicarán a este control. Este número debe ser no negativo y especificar un atributo para un control estático que sea válido para la selección de ubicación en una tabla. Para obtener información sobre los valores numéricos que se escriben en este campo, vea el atributo concreto en [Atributos de control](control-attributes.md).

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Esta columna contiene una cadena localizable que se usa para establecer el texto inicial en el control si el control muestra texto. La cadena se trunca si el texto es demasiado largo para caber en el control. Esta columna contiene una clave en la [tabla Binary](binary-table.md) si el control es un botón de inserción o una casilla que contiene un icono o mapa de bits. No es posible mostrar texto y una imagen en el mismo botón. Es posible que esta columna se haya dejado en blanco.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los valores enteros de x, y, width y height se encuentran en las unidades [del instalador,](installer-units.md)no en las unidades de diálogo. Una unidad del instalador es igual a la duodécima altura del tamaño de fuente MS Sans Serif de 10 puntos. Las coordenadas de los controles son relativas al control no al cuadro de diálogo.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE95](ice95.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
</dt> </dl>

 

 



