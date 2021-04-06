---
description: Las líneas de un cuadro de lista no se tratan como controles individuales, pero forman parte de un cuadro de lista que funciona como un control. La tabla ListBox define los valores para todos los cuadros de lista.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: Tabla ListBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002250"
---
# <a name="listbox-table"></a>Tabla ListBox

Las líneas de un cuadro de lista no se tratan como controles individuales, pero forman parte de un cuadro de lista que funciona como un control. La tabla ListBox define los valores para todos los cuadros de lista.

La tabla ListBox tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Propiedad | [Identificador](identifier.md) | Y   | N        |
| Pedido    | [Entero](integer.md)       | Y   | N        |
| Value    | [Formatea](formatted.md)   | N   | N        |
| Texto     | [Formatea](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Propiedad con nombre que se va a asociar a este elemento. Todos los elementos vinculados a la misma propiedad forman parte del mismo cuadro de lista.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden
</dt> <dd>

Un entero positivo que se usa para determinar el orden de los elementos que aparecen en un solo cuadro de lista. Si el cuadro de lista se define como ordenado, todos los elementos deben tener un valor de orden. Los enteros no tienen que ser consecutivos. Si el cuadro de lista se define como sin ordenar, se omitirá esta columna.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Cadena de valor asociada a este elemento. Al seleccionar la línea, se establece la propiedad asociada en este valor.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Negrita
</dt> <dd>

Texto visible localizable que se va a asignar al elemento. Si falta esta entrada o toda la columna, el valor predeterminado del texto es la entrada correspondiente en Value.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) da formato al contenido de los campos de texto y de valor cuando se crea el control, por lo que puede contener cualquier expresión que pueda interpretar la función **MsiFormatRecord** . El formato solo se produce cuando se crea el control y no se actualiza si se modifica una propiedad implicada en la expresión durante la vida del control.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE46](ice46.md)  
</dl>

 

 



