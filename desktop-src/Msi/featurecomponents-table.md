---
description: La tabla FeatureComponents define la relación entre las características y los componentes de. Para cada característica, en esta tabla se enumeran todos los componentes que componen esa característica.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Tabla FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811821"
---
# <a name="featurecomponents-table"></a>Tabla FeatureComponents

La tabla FeatureComponents define la relación entre las características y los componentes de. Para cada característica, en esta tabla se enumeran todos los componentes que componen esa característica.

La tabla FeatureComponents tiene las columnas siguientes.



| Columna      | Tipo                         | Clave | Nullable |
|-------------|------------------------------|-----|----------|
| Característica\_   | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_
</dt> <dd>

Una clave externa en la primera columna de la [tabla](feature-table.md)de características.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_
</dt> <dd>

Una clave externa en la primera columna de la [tabla de componentes](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Existe un límite máximo de 1600 componentes por característica.

Dos o más características pueden compartir los componentes, es decir, se puede hacer referencia al mismo componente a través de más de una característica.

Se hace referencia a esta tabla cuando se ejecuta la acción [PublishFeatures](publishfeatures-action.md) o la [acción UnpublishFeatures](unpublishfeatures-action.md) .

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE21](ice21.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE47](ice47.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE69](ice69.md)  
</dl>

 

 



