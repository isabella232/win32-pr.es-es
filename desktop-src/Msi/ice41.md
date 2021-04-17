---
description: ICE41 valida que las entradas de las tablas de clase y extensión hacen referencia a las entradas de la tabla de componentes que implementan el objeto de clase o la extensión del componente.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652814"
---
# <a name="ice41"></a>ICE41

ICE41 valida que las entradas de las tablas de [clase](class-table.md) y [extensión](extension-table.md) hacen referencia a las entradas de la [tabla de componentes](component-table.md) que implementan el objeto de clase o la extensión del componente.

## <a name="result"></a>Resultado

ICE41 publica un error si hay una característica que no contiene el componente que implementa la extensión o el objeto de clase.

## <a name="example"></a>Ejemplo

ICE41 notifica los siguientes errores para el ejemplo que se muestra.



| Error ICE41                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| {00000000-0000-0000-0000-0000000000000}La clase hace referencia a la característica característica2 y al componente Component1, pero el componente no está asociado a esa característica en la tabla FeatureComponents. | Hay una característica que no contiene el componente que implementa el objeto de clase. Esto significa que el instalador no instala el componente con la característica y que el anuncio puede no funcionar según lo esperado. Para corregir este error, cambie la entrada en la \_ columna característica de la entrada de la [tabla de clases](class-table.md) para que haga referencia a una característica que instala el componente enumerado en la columna componente \_ o cambie la característica y el componente asociados en la [tabla FeatureComponents](featurecomponents-table.md).<br/>          |
| Extension. Yip hace referencia a la característica Feature1 y al componente Component2, pero el componente no está asociado a esa característica en la tabla FeatureComponents.                                | Hay una característica que no contiene el componente que implementa la extensión. Esto significa que el instalador no instala el componente con la característica y que el anuncio puede no funcionar según lo esperado. Para corregir este error, cambie la entrada en la \_ columna característica de la entrada de la [tabla de extensión](extension-table.md) para que haga referencia a una característica que instala el componente enumerado en la \_ columna componente o cambie la característica y el componente asociados en la [tabla FeatureComponents](featurecomponents-table.md).<br/> |



 

[Tabla FeatureComponents](featurecomponents-table.md) (parcial)



| Característica\_ |
|-----------|
| Feature1  |
| Característica2  |



 

[Tabla de clases](class-table.md) (parcial)



| CLSID                                  | Componente\_ | Característica\_ |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | Component1  | Característica2  |



 

[Tabla de clases](class-table.md) (parcial)



| Extensión | Componente\_ | Característica\_ |
|-----------|-------------|-----------|
| .yip      | Component2  | Feature1  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




