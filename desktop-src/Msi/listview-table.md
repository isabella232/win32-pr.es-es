---
description: Las líneas de un control ListView no se tratan como controles individuales, pero forman parte de un control ListView que funciona como un control. La tabla ListView define los valores para todos los controles ListView.
ms.assetid: 0da4eab9-cabc-4bcc-8267-4aa1cd79e78b
title: Tabla ListView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e7296db9f71a7c40550fdcaab18d8f0d0f41f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687370"
---
# <a name="listview-table"></a>Tabla ListView

Las líneas de un control ListView no se tratan como controles individuales, pero forman parte de un control ListView que funciona como un control. La tabla ListView define los valores para todos los controles ListView.

La tabla ListView tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Propiedad | [Identificador](identifier.md) | Y   | N        |
| Pedido    | [Entero](integer.md)       | Y   | N        |
| Value    | [Formatea](formatted.md)   | N   | N        |
| Texto     | [Formatea](formatted.md)   | N   | Y        |
| Binary\_ | [Identificador](identifier.md) | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Propiedad con nombre que se va a asociar a este elemento. Todos los elementos vinculados a la misma propiedad forman parte del mismo ListView.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden
</dt> <dd>

Un entero positivo que se usa para determinar el orden de los elementos que aparecen en una única lista de ListView. Los enteros no tienen que ser consecutivos. Si un control ListView se define como ordenado, todos los elementos deben tener un valor de ordenación. Si ListView se define como sin ordenar, se omite esta columna.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Cadena de valor asociada a este elemento. Al seleccionar la línea, se establece la propiedad asociada en este valor.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Negrita
</dt> <dd>

Texto visible y localizable que se va a asignar al elemento. Si falta esta entrada o toda la columna, el valor predeterminado del texto es la entrada correspondiente en Value.

</dd> <dt>

<span id="Binary_"></span><span id="binary_"></span><span id="BINARY_"></span>Binario\_
</dt> <dd>

Datos de imagen para el icono. Se trata de una clave externa de la [tabla binaria](binary-table.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) da formato al contenido de los campos de texto y de valor cuando se crea el control, por lo que puede contener cualquier expresión que pueda interpretar la función MsiFormatRecord. El formato solo se produce cuando se crea el control y no se actualiza si se modifica una propiedad implicada en la expresión durante la vida del control.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE32](ice32.md)  
</dl>

 

 



