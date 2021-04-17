---
description: ICE21 valida que todos los componentes de la tabla de componentes pertenezcan a una característica. Usa la tabla FeatureComponents para comprobar esta asignación.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667762"
---
# <a name="ice21"></a>ICE21

ICE21 valida que todos los componentes de la [tabla de componentes](component-table.md) pertenezcan a una característica. Usa la [tabla FeatureComponents](featurecomponents-table.md) para comprobar esta asignación.

## <a name="result"></a>Resultado

ICE21 envía un mensaje de error si el paquete de instalación contiene un componente que no pertenece a una característica.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente, ICE21 envía un mensaje de error que indica que el componente Comp1 no se asigna a ninguna característica.

[Tabla de componentes](component-table.md) (parcial)



| Componente |
|-----------|
| Comp1     |
| Comp2     |



 

[Tabla FeatureComponents](featurecomponents-table.md) (parcial)



| Característica  | Componente |
|----------|-----------|
| Feature1 | Comp2     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



