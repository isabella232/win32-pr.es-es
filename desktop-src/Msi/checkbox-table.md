---
description: La tabla CheckBox muestra los valores de las casillas.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: Tabla CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666999"
---
# <a name="checkbox-table"></a>Tabla CheckBox

La tabla CheckBox muestra los valores de las casillas.

La tabla CheckBox tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Propiedad | [Identificador](identifier.md) | Y   | N        |
| Value    | [Formatea](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Propiedad con nombre que se va a asociar a este elemento.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Cadena de valor asociada a este elemento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si la casilla está activada, la propiedad correspondiente se establece en el valor especificado. Si no hay ningún valor especificado o esta tabla no existe, la propiedad se establece en su valor original cuando la casilla está activada. Si el valor original es null, la propiedad se establece en "1".

La función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) da formato al contenido de la columna de valor cuando se crea el control. Por lo tanto, puede contener cualquier expresión que la función **MsiFormatRecord** pueda interpretar. Solo se da formato a la columna valor cuando se crea el control y no se actualiza si una propiedad implicada en una expresión se modifica durante la vida del control.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



