---
description: ICE95 comprueba la tabla de control y la tabla BBControl para comprobar que los controles de los paneles caben en todos los paneles.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074503"
---
# <a name="ice95"></a>ICE95

ICE95 comprueba la tabla [de control y](control-table.md) la tabla [BBControl](bbcontrol-table.md) para comprobar que los controles de los paneles caben en todos los paneles.

## <a name="result"></a>Resultado

Si se cumple alguna de las siguientes condiciones, un control Descontrol no cabe en un cuadro. ICE95 publica las advertencias siguientes.



| Advertencia de ICE95                                                                                                                                                                                                              | Descripción                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de paneles de la tabla Control. La coordenada X supera el límite del ancho de control mínimo %s                   | La coordenada X del control está fuera del ancho del borde.                          |
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de paneles de la tabla Control. La coordenada Y supera el límite de la altura de control mínima %s                  | La coordenada Y del control está debajo de la parte inferior de la fila.                           |
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de paneles de la tabla Control. La coordenada X y el ancho combinados superan el ancho de control mínimo %s   | La coordenada X del control más el ancho del control está fuera del ancho del borde. |
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de paneles de la tabla Control. La coordenada Y y el alto combinados superan la altura mínima del control de los paneles %s. | La coordenada Y del control más la altura del control está debajo de la parte inferior de la barra. |



 

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
| control1 | Cartelera | 300   | 100    |
| Control2 | Cartelera | 100   | 300    |



 

[Tabla BBControl](bbcontrol-table.md)



| Cartelera\_ | BBControl  | X   | Y   | Ancho | Alto |
|-------------|------------|-----|-----|-------|--------|
| yádes1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| yádes1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| yádes1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| yádes1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



