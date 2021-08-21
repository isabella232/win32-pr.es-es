---
description: Las líneas de un cuadro combinado no se tratan como controles individuales; forman parte de un único cuadro combinado que funciona como control. En esta tabla se enumeran los valores de cada cuadro combinado.
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: Tabla ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea20677ab6ede02f76a1061d5f715eb0b8d6d87a1744d1eb89b7e0918a018e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380300"
---
# <a name="combobox-table"></a>Tabla ComboBox

Las líneas de un cuadro combinado no se tratan como controles individuales; forman parte de un único cuadro combinado que funciona como control. En esta tabla se enumeran los valores de cada cuadro combinado.

La tabla ComboBox tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Propiedad | [Identificador](identifier.md) | Y   | N        |
| Pedido    | [Entero](integer.md)       | Y   | N        |
| Valor    | [Formato](formatted.md)   | N   | N        |
| Texto     | [Texto](text.md)             | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Propiedad con nombre que se va a vincular a este elemento. Todos los elementos vinculados a la misma propiedad se convierten en parte del mismo cuadro combinado.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden
</dt> <dd>

Entero positivo que se usa para determinar el orden de los elementos que aparecen en una sola lista de cuadros combinados. Los enteros no tienen que ser consecutivos. Si un cuadro combinado se define como ordenado, todos los elementos deben tener un valor Order. Si el cuadro combinado se define como desordenado, se omite esta columna.

Solo números positivos.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Cadena de valor asociada a este elemento. Al seleccionar esta línea del cuadro combinado, se establece la propiedad asociada (especificada en Propiedad) en este valor.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Texto visible y localizable que se va a asignar al elemento. Si falta esta entrada o toda la columna, el texto tiene como valor predeterminado la entrada en Valor.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El contenido de los campos Value y Text tiene el formato de la función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) cuando se crea el control, por lo que pueden contener cualquier expresión que la función **MsiFormatRecord** pueda interpretar. El formato solo se produce cuando se crea el control y no se actualiza si una propiedad implicada en la expresión se modifica durante la vida del control.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE46](ice46.md)  
</dl>

 

 



