---
description: ICE22 usa la tabla FeatureComponents para validar la asignación de características y componentes a los que se hace referencia en la tabla PublishComponent.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667761"
---
# <a name="ice22"></a>ICE22

ICE22 usa la [tabla FeatureComponents](featurecomponents-table.md) para validar la asignación de características y componentes a los que se hace referencia en la [tabla PublishComponent](publishcomponent-table.md).

## <a name="result"></a>Resultado

ICE22 envía un mensaje de error si las características y los componentes se asignan de forma incorrecta en la [tabla PublishComponent](publishcomponent-table.md).

## <a name="example"></a>Ejemplo

En el ejemplo siguiente, ICE22 envía un error que {00000003-0004-0000-0000-624474732465} no tiene la asignación correcta para las columnas de característica \_ y componente \_ .

[Tabla PublishComponent](publishcomponent-table.md) (parcial)



| ComponentId                            | Característica\_ | Componente\_ |
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

 

 



