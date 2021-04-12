---
description: ICE95 comprueba la tabla de control y la tabla BBControl para comprobar que los controles de la cartelera caben en todas las cartelera.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278455"
---
# <a name="ice95"></a>ICE95

ICE95 comprueba la tabla de [control](control-table.md) y la [tabla BBControl](bbcontrol-table.md) para comprobar que los controles de la cartelera caben en todas las cartelera.

## <a name="result"></a>Resultado

Si se cumple alguna de las siguientes condiciones, el control de la cartelera no cabe en una cartelera. ICE95 expone las siguientes advertencias.



| ADVERTENCIA de ICE95                                                                                                                                                                                                              | Descripción                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de la cartelera de la tabla de control. La coordenada X supera el límite del ancho mínimo del control de la cartelera% s                   | La coordenada X del control está fuera del ancho de la cartelera.                          |
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de la cartelera de la tabla de control. La coordenada Y supera el límite de la altura del control de la cartelera mínima% s                  | La coordenada Y del control está debajo de la parte inferior de la cartelera.                           |
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de la cartelera de la tabla de control. La coordenada X y el ancho combinados juntos superan el ancho mínimo del control de la cartelera% s   | La coordenada X del control más el ancho del control está fuera del ancho de la cartelera. |
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de la cartelera de la tabla de control. La coordenada Y y el alto combinado juntos superan el alto del control de la cartelera mínimo% s | La coordenada Y del control más el alto del control está por debajo de la parte inferior de la cartelera. |



 

## <a name="example"></a>Ejemplo

ICE95 notifica las siguientes advertencias para el ejemplo:

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

Tabla de control (parcial) (parcial)



| Control  | Tipo      | Ancho | Alto |
|----------|-----------|-------|--------|
| control1 | Valla | 300   | 100    |
| Control2 | Valla | 100   | 300    |



 

[Tabla BBControl](bbcontrol-table.md)



| Valla\_ | BBControl  | X   | Y   | Ancho | Alto |
|-------------|------------|-----|-----|-------|--------|
| billboard1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| billboard1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| billboard1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| billboard1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



