---
description: Si una tabla del módulo merge aparece en la tabla ModuleIgnoreTable, no se combina en el archivo .msi combinación.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: ModuleIgnoreTable Table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261156"
---
# <a name="moduleignoretable-table"></a>ModuleIgnoreTable Table

Si una tabla del módulo merge aparece en la tabla ModuleIgnoreTable, no se combina en el archivo .msi combinación. Si la tabla ya existe en el .msi, la combinación no la modifica. Por lo tanto, las tablas de ModuleIgnoreTable pueden contener datos innecesarios después de la combinación.

La tabla ModuleIgnoreTable tiene las columnas siguientes.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Tabla  | [Identificador](identifier.md) | S   | No       |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Mesa
</dt> <dd>

Nombre de la tabla del módulo de combinación que no se va a combinar en el archivo .msi combinación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para minimizar el tamaño del archivo .msm, se recomienda que los desarrolladores quiten las tablas no usadas de los módulos destinados a la redistribución en lugar de enumerar estas tablas en la tabla ModuleIgnoreTable.

 

 



