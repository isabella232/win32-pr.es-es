---
description: ICE08 valida que la tabla Component no contiene GUID duplicados. Cada componente debe tener un GUID único. No se realiza ninguna validación si la tabla Component no existe.
ms.assetid: c8ff53f3-6587-479d-afb8-b09d0df3b673
title: ICE08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051f32aa983fdae39fc3717d3c9036b542f14369
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074673"
---
# <a name="ice08"></a>ICE08

ICE08 valida que la tabla [Component](component-table.md) no contiene GUID [duplicados.](guid.md) Cada componente debe tener un GUID único. No se realiza ninguna validación si la tabla Component no existe.

## <a name="result"></a>Resultado

ICE08 publica un mensaje de error si dos o más entradas de la columna ComponentId de la tabla Component contienen el mismo GUID.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente, ICE08 publicaría un mensaje que indica que los componentes Rojo y Verde tienen GUID duplicados.

[Tabla de componentes](component-table.md) (parcial)



| Componente | Componentid                            |
|-----------|----------------------------------------|
| Rojo       | {0000000A-0003-0000-0000-624474736554} |
| Azul      | {0000000A-0003-0000-0000-624474736354} |
| Verde     | {0000000A-0003-0000-0000-624474736554} |



 

Para corregir este error, cambie cualquiera de los GUID duplicados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



