---
description: ICE47 comprueba la característica y las tablas FeatureComponents para ver si hay características con 1600 o más componentes.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276718"
---
# <a name="ice47"></a>ICE47

ICE47 comprueba la [característica](feature-table.md) y las tablas [FeatureComponents](featurecomponents-table.md) para ver si hay características con 1600 o más componentes.

## <a name="result"></a>Resultado

ICE47 envía un mensaje de error si una característica supera el límite máximo de 1600 componentes por característica.

## <a name="example"></a>Ejemplo

ICE47 notificaría la siguiente ADVERTENCIA:

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

[Tabla de características](feature-table.md) (parcial)



| Característica  |
|----------|
| Feature1 |



 

[Tabla FeatureComponents](featurecomponents-table.md) (parcial)



| Acción   | Condición     |
|----------|---------------|
| Feature1 | Component1    |
| Feature1 | Component1600 |



 

Para corregir esta advertencia, intente dividir la característica en varias características.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



