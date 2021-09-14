---
description: Las líneas de un cuadro de lista no se tratan como controles individuales, pero forman parte de un cuadro de lista que funciona como un control . La tabla ListBox define los valores de todos los cuadros de lista.
ms.assetid: 1963adcf-f682-4371-ab44-f91e90105dc0
title: ListBox (tabla)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f60fb6ac48860c7893b0320b54e6e54dcf1691
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071953"
---
# <a name="listbox-table"></a>ListBox (tabla)

Las líneas de un cuadro de lista no se tratan como controles individuales, pero forman parte de un cuadro de lista que funciona como un control . La tabla ListBox define los valores de todos los cuadros de lista.

La tabla ListBox tiene las siguientes columnas.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Propiedad. | [Identificador](identifier.md) | Y   | N        |
| Pedido    | [Entero](integer.md)       | Y   | N        |
| Value    | [Formato](formatted.md)   | N   | N        |
| Texto     | [Formato](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Propiedad con nombre que se va a vincular a este elemento. Todos los elementos vinculados a la misma propiedad forman parte del mismo cuadro de lista.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden
</dt> <dd>

Entero positivo que se usa para determinar el orden de los elementos que aparecen en un único cuadro de lista. Si el cuadro de lista se define como ordenado, todos los elementos deben tener un valor Order. Los enteros no tienen que ser consecutivos. Si el cuadro de lista se define como desordenado, se omite esta columna.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Cadena de valor asociada a este elemento. Al seleccionar la línea se establece la propiedad asociada en este valor.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Texto visible localizable que se va a asignar al elemento. Si falta esta entrada o toda la columna, el texto tiene como valor predeterminado la entrada correspondiente en Valor.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El contenido de los campos Value y Text tiene el formato de la función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) cuando se crea el control, por lo que pueden contener cualquier expresión que la **función MsiFormatRecord** pueda interpretar. El formato solo se produce cuando se crea el control y no se actualiza si una propiedad implicada en la expresión se modifica durante la vida del control.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE46](ice46.md)  
</dl>

 

 



