---
description: ICE22 usa la tabla FeatureComponents para validar la asignación de características y componentes a los que se hace referencia en la tabla PublishComponent.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 177fcef5441e5b82738c76face70427cc6865ae59c11542fca080b3dc521c5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529025"
---
# <a name="ice22"></a>ICE22

ICE22 usa la [tabla FeatureComponents para](featurecomponents-table.md) validar la asignación de características y componentes a los que se hace referencia en [la tabla PublishComponent](publishcomponent-table.md).

## <a name="result"></a>Resultado

ICE22 publica un mensaje de error si las características y componentes se asignan incorrectamente en la [tabla PublishComponent](publishcomponent-table.md).

## <a name="example"></a>Ejemplo

En el ejemplo siguiente, ICE22 publica un error que no tiene la asignación {00000003-0004-0000-0000-624474732465} correcta para las columnas Feature y \_ \_ Component.

[Tabla PublishComponent](publishcomponent-table.md) (parcial)



| Componentid                            | Característica\_ | Componente\_ |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | Feat1     | Comp1       |
| {00000003-0004-0000-0000-624474732465} | Feat1     | Comp2       |



 

[Tabla FeatureComponents](featurecomponents-table.md) (parcial)



| Característica\_ | Componente\_ |
|-----------|-------------|
| Feat1     | Comp1       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



