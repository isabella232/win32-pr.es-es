---
description: Si una tabla del módulo de combinación aparece en la tabla ModuleIgnoreTable, no se combina en el archivo. msi.
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: Tabla ModuleIgnoreTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7b0191f616eced187411a148e40e0ae6575cca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278810"
---
# <a name="moduleignoretable-table"></a>Tabla ModuleIgnoreTable

Si una tabla del módulo de combinación aparece en la tabla ModuleIgnoreTable, no se combina en el archivo. msi. Si la tabla ya existe en el archivo. msi, la combinación no la modifica. Por tanto, las tablas de ModuleIgnoreTable pueden contener datos innecesarios después de la combinación.

La tabla ModuleIgnoreTable tiene las columnas siguientes.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Tabla  | [Identificador](identifier.md) | S   | No       |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Cuadro
</dt> <dd>

Nombre de la tabla del módulo de combinación que no se va a combinar en el archivo. msi.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para minimizar el tamaño del archivo. MSM, se recomienda que los desarrolladores quiten las tablas sin usar de los módulos destinados a la redistribución en lugar de enumerar estas tablas en la tabla ModuleIgnoreTable.

 

 



