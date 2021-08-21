---
description: ICE21 valida que todos los componentes de la tabla Component pertenecen a una característica. Usa la tabla FeatureComponents para comprobar esta asignación.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c5c517bd41c7d777f327606b3672f90b57a821dbbef028fa985acd043e6768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529035"
---
# <a name="ice21"></a>ICE21

ICE21 valida que todos los componentes de la [tabla Component](component-table.md) pertenecen a una característica. Usa la [tabla FeatureComponents para](featurecomponents-table.md) comprobar esta asignación.

## <a name="result"></a>Resultado

ICE21 envía un mensaje de error si el paquete de instalación contiene un componente que no pertenece a una característica.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente, ICE21 publica un mensaje de error que indica que el componente Comp1 no se asigna a ninguna característica.

[Tabla de componentes](component-table.md) (parcial)



| Componente |
|-----------|
| Comp1     |
| Comp2     |



 

[Tabla FeatureComponents](featurecomponents-table.md) (parcial)



| Característica  | Componente |
|----------|-----------|
| Característica 1 | Comp2     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



