---
description: Las líneas de un cuadro combinado no se tratan como controles individuales; forman parte de un único cuadro combinado que funciona como un control. En esta tabla se enumeran los valores de cada cuadro combinado.
ms.assetid: 1d3566ac-e95d-48ed-bce4-fb4604d5f762
title: Tabla ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e209ac8a7c27c36fd5c1bbd3c97822617c48f5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652894"
---
# <a name="combobox-table"></a>Tabla ComboBox

Las líneas de un cuadro combinado no se tratan como controles individuales; forman parte de un único cuadro combinado que funciona como un control. En esta tabla se enumeran los valores de cada cuadro combinado.

La tabla ComboBox tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Propiedad | [Identificador](identifier.md) | Y   | N        |
| Pedido    | [Entero](integer.md)       | Y   | N        |
| Value    | [Formatea](formatted.md)   | N   | N        |
| Texto     | [Texto](text.md)             | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Propiedad con nombre que se va a asociar a este elemento. Todos los elementos vinculados a la misma propiedad forman parte del mismo cuadro combinado.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden
</dt> <dd>

Un entero positivo que se usa para determinar el orden de los elementos que aparecen en una sola lista de cuadro combinado. Los enteros no tienen que ser consecutivos. Si se define un cuadro combinado como ordenado, todos los elementos deben tener un valor de orden. Si el cuadro combinado se define como sin ordenar, se omite esta columna.

Solo números positivos.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Cadena de valor asociada a este elemento. Al seleccionar esta línea del cuadro combinado, se establece la propiedad asociada (especificada en la propiedad) en este valor.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Negrita
</dt> <dd>

Texto visible y localizable que se va a asignar al elemento. Si falta esta entrada o toda la columna, el valor predeterminado del texto es la entrada de Value.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) da formato al contenido de los campos de texto y de valor cuando se crea el control, por lo que puede contener cualquier expresión que pueda interpretar la función **MsiFormatRecord** . El formato solo se produce cuando se crea el control y no se actualiza si se modifica una propiedad implicada en la expresión durante la vida del control.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE46](ice46.md)  
</dl>

 

 



