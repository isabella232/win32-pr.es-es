---
description: En la tabla BBControl se muestran los controles que se van a mostrar en cada cartelera.
ms.assetid: 2ab31a32-6d33-46b7-a295-199560efa7fb
title: Tabla BBControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfebbdbc474ef88cbf26f34555deb4874840d005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667021"
---
# <a name="bbcontrol-table"></a>Tabla BBControl

En la tabla BBControl se muestran los controles que se van a mostrar en cada cartelera.

La tabla BBControl tiene las columnas siguientes.



| Columna      | Tipo                               | Clave | Nullable |
|-------------|------------------------------------|-----|----------|
| Valla\_ | [Identificador](identifier.md)       | Y   | N        |
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

<span id="Billboard_"></span><span id="billboard_"></span><span id="BILLBOARD_"></span>Valla\_
</dt> <dd>

Nombre de la cartelera.

Clave externa para la columna uno de la tabla de la [cartelera](billboard-table.md).

</dd> <dt>

<span id="BBControl"></span><span id="bbcontrol"></span><span id="BBCONTROL"></span>BBControl
</dt> <dd>

Nombre del control. Este nombre debe ser único dentro de una cartelera, pero se puede repetir en distintas cartelera. Esta columna combinada con la columna de la cartelera forma \_ la clave principal de la tabla.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente
</dt> <dd>

Tipo del control. Solo los controles estáticos, como un [texto](text-control.md), un [mapa de bits](bitmap-control.md), un [icono](icon-control.md)o un control personalizado, se pueden colocar en una cartelera. Para obtener una lista completa de los controles, vea la sección [controles](controls.md) .

</dd> <dt>

<span id="X"></span><span id="x"></span>X1
</dt> <dd>

Coordenada horizontal de la esquina superior izquierda del límite rectangular del control. Las unidades son [unidades de instalador](installer-units.md). Esta coordenada se mide en relación con el control de la cartelera y no con respecto al cuadro de diálogo. Use solo números no negativos.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Sí
</dt> <dd>

Coordenada vertical de la esquina superior izquierda del límite rectangular del control. Las unidades son [unidades de instalador](installer-units.md). Esta coordenada se mide en relación con el control de la cartelera y no con respecto al cuadro de diálogo. Este número no debe ser negativo.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Ancho
</dt> <dd>

Ancho del límite rectangular del control. Las unidades son [unidades de instalador](installer-units.md). Este número no debe ser negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Alto
</dt> <dd>

Alto del límite rectangular del control. Las unidades son [unidades de instalador](installer-units.md). Este número no debe ser negativo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus
</dt> <dd>

Una palabra de 32 bits que especifica las marcas de atributo que se van a aplicar a este control. Este número no debe ser negativo y especificar un atributo para un control estático que sea válido para la selección de ubicación en una cartelera. Para obtener información sobre los valores numéricos que se van a escribir en este campo, vea el atributo concreto bajo [atributos de control](control-attributes.md).

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Negrita
</dt> <dd>

Esta columna contiene una cadena localizable que se usa para establecer el texto inicial del control si el control muestra texto. La cadena se trunca si el texto es demasiado largo para caber en el control. Esta columna contiene una clave en la [tabla binaria](binary-table.md) si el control es un botón de inserción o una casilla que contiene un icono o un mapa de bits. No es posible mostrar texto y una imagen en el mismo botón. Esta columna puede dejarse en blanco.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los valores enteros para x, y, ancho y alto se encuentran en las [unidades de instalador](installer-units.md), no en las unidades de cuadro de diálogo. Una unidad de instalador es igual a una duodécima el alto del tamaño de fuente MS Sans Serif de 10 puntos. Las coordenadas de los controles son relativas al control de la cartelera, no al cuadro de diálogo.

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

 

 



