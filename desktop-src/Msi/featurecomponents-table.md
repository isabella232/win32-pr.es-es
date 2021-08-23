---
description: La tabla FeatureComponents define la relación entre características y componentes. Para cada característica, en esta tabla se enumeran todos los componentes que la conste.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Tabla FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7635a43784ee7e8fbb71c7161bb07d39ffe5238177ea2a7cdaabdeb18dc41e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430875"
---
# <a name="featurecomponents-table"></a>Tabla FeatureComponents

La tabla FeatureComponents define la relación entre características y componentes. Para cada característica, en esta tabla se enumeran todos los componentes que la conste.

La tabla FeatureComponents tiene las siguientes columnas.



| Columna      | Tipo                         | Key | Nullable |
|-------------|------------------------------|-----|----------|
| Característica\_   | [Identificador](identifier.md) | Y   | N        |
| Componente\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Característica\_
</dt> <dd>

Clave externa en la primera columna de la tabla [Feature](feature-table.md).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Clave externa en la primera columna de la [tabla Component](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Hay un límite máximo de 1600 componentes por característica.

Los componentes se pueden compartir entre dos o más características, es decir, más de una característica puede hacer referencia al mismo componente.

Se hace referencia a esta tabla cuando se ejecuta la [acción PublishFeatures](publishfeatures-action.md) o la acción [UnpublishFeatures.](unpublishfeatures-action.md)

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

 

 



