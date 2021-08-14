---
description: ICE95 comprueba la tabla De control y la tabla BBControl para comprobar que los controles de la bolsa caben en todos los paneles.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f0f7d44554385c33648036f314406971193afc079b5aa8e72cf595695797ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315265"
---
# <a name="ice95"></a>ICE95

ICE95 comprueba la tabla [De control y](control-table.md) la tabla [BBControl](bbcontrol-table.md) para comprobar que los controles de la bolsa caben en todos los paneles.

## <a name="result"></a>Resultado

Si se cumple alguna de las condiciones siguientes, un control de la ciudad no cabe en un panel. ICE95 publica las siguientes advertencias.



| Advertencia de ICE95                                                                                                                                                                                                              | Descripción                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de paneles de la tabla Control. La coordenada X supera el límite del ancho mínimo de control de la banda %s                   | La coordenada X del control está fuera del ancho del panel.                          |
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de paneles de la tabla Control. La coordenada Y supera el límite de la altura mínima del control de ciudad %s                  | La coordenada Y del control está debajo de la parte inferior del panel.                           |
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de paneles de la tabla Control. La coordenada X y el ancho combinados superan el ancho de control mínimo %s   | La coordenada X del control más el ancho del control está fuera del ancho del panel. |
| El elemento BBControl ' \[ 1 \] . \[ 2 \] ' en la tabla BBControl no cabe en todos los controles de paneles de la tabla Control. La coordenada Y y el alto combinados superan el alto mínimo del control de la ciudad %s. | La coordenada Y del control más el alto del control se encuentra debajo de la parte inferior del panel. |



 

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
| yónctese1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| yónctese1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| yónctese1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| yónctese1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



