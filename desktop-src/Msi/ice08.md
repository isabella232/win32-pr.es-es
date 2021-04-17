---
description: ICE08 valida que la tabla de componentes no contiene GUID duplicados. Cada componente debe tener un GUID único. No se realiza ninguna validación si la tabla de componentes no existe.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667774"
---
# <a name="ice08"></a>ICE08

ICE08 valida que la [tabla de componentes](component-table.md) no contiene [GUID](guid.md)duplicados. Cada componente debe tener un GUID único. No se realiza ninguna validación si la tabla de componentes no existe.

## <a name="result"></a>Resultado

ICE08 envía un mensaje de error si dos o más entradas de la columna ComponentId de la tabla de componentes contienen el mismo GUID.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente, ICE08 publicaría un mensaje que indica que los componentes rojo y verde tienen GUID duplicados.

[Tabla de componentes](component-table.md) (parcial)



| Componente | ComponentId                            |
|-----------|----------------------------------------|
| Rojo       | {0000000A-0003-0000-0000-624474736554} |
| Azul      | {0000000A-0003-0000-0000-624474736354} |
| Verde     | {0000000A-0003-0000-0000-624474736554} |



 

Para corregir este error, cambie uno de los GUID duplicados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



