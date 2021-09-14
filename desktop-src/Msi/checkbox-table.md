---
description: En la tabla CheckBox se enumeran los valores de las casillas.
ms.assetid: 6881f358-74af-4160-ac69-36e848865ac0
title: CheckBox Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3600b741543a88e7ded71cd385a56b499c8ef516
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158922"
---
# <a name="checkbox-table"></a>CheckBox Table

En la tabla CheckBox se enumeran los valores de las casillas.

La tabla CheckBox tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Propiedad. | [Identificador](identifier.md) | Y   | N        |
| Value    | [Formato](formatted.md)   | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Propiedad con nombre que se va a vincular a este elemento.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Cadena de valor asociada a este elemento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si la casilla está activada, la propiedad correspondiente se establece en el valor especificado. Si no se especifica ningún valor o esta tabla no existe, la propiedad se establece en su valor original cuando se selecciona la casilla. Si el valor original es NULL, la propiedad se establece en "1".

El contenido de la columna Value tiene el formato de la [**función MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) cuando se crea el control. Por lo tanto, puede contener cualquier expresión que **la función MsiFormatRecord** pueda interpretar. La columna Valor solo tiene formato cuando se crea el control y no se actualiza si se modifica una propiedad implicada en una expresión durante la vida del control.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



