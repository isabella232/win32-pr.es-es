---
description: Las líneas de una vista de lista no se tratan como controles individuales, pero forman parte de una vista de lista que funciona como un control . La tabla ListView define los valores de todas las vistas de lista.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: ListView (tabla)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074424"
---
# <a name="listview-table"></a>ListView (tabla)

Las líneas de una vista de lista no se tratan como controles individuales, pero forman parte de una vista de lista que funciona como un control . La tabla ListView define los valores de todas las vistas de lista.

La tabla ListView tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Propiedad. | [Identificador](identifier.md) | Y   | N        |
| Pedido    | [Entero](integer.md)       | Y   | N        |
| Value    | [Formato](formatted.md)   | N   | N        |
| Texto     | [Formato](formatted.md)   | N   | Y        |
| Binary\_ | [Identificador](identifier.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Propiedad con nombre que se va a vincular a este elemento. Todos los elementos vinculados a la misma propiedad se convierten en parte de la misma vista de lista.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden
</dt> <dd>

Entero positivo que se usa para determinar el orden de los elementos que aparecen en una única lista de vistas de lista. Los enteros no tienen que ser consecutivos. Si una vista de lista se define como ordenada, todos los elementos deben tener un valor ordering. Si la vista de lista se define como desordenada, se omite esta columna.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Cadena de valor asociada a este elemento. Al seleccionar la línea, se establece la propiedad asociada en este valor.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Texto visible y localizable que se va a asignar al elemento. Si falta esta entrada o toda la columna, el texto tiene como valor predeterminado la entrada correspondiente en Valor.

</dd> <dt>

<span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binario\_
</dt> <dd>

Los datos de imagen del icono. Se trata de una clave externa para la [tabla binaria](binary-table.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El contenido de los campos Value y Text tiene el formato de la función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) cuando se crea el control, por lo que pueden contener cualquier expresión que la función MsiFormatRecord pueda interpretar. El formato solo se produce cuando se crea el control y no se actualiza si una propiedad implicada en la expresión se modifica durante la vida del control.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
</dl>

 

 



