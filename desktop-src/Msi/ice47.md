---
description: ICE47 comprueba las tablas Feature y FeatureComponents en busca de características con 1600 componentes o más.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdcf1f71af9bb8784c15b159836d329a94e7e6f33b34c31cbba72f9b31349a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381955"
---
# <a name="ice47"></a>ICE47

ICE47 comprueba las [tablas Feature](feature-table.md) [y FeatureComponents](featurecomponents-table.md) en busca de características con 1600 componentes o más.

## <a name="result"></a>Resultado

ICE47 envía un mensaje de error si una característica supera el límite máximo de 1600 componentes por característica.

## <a name="example"></a>Ejemplo

ICE47 notificaría la advertencia siguiente:

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

[Tabla de características](feature-table.md) (parcial)



| Característica  |
|----------|
| Característica 1 |



 

[Tabla FeatureComponents](featurecomponents-table.md) (parcial)



| Acción   | Condición     |
|----------|---------------|
| Característica 1 | Componente1    |
| Característica 1 | Component1600 |



 

Para corregir esta advertencia, intente dividir la característica en varias características.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



