---
description: ICE41 valida que las entradas de las tablas Class y Extension hacen referencia a las entradas de la tabla Component que implementan el objeto de clase o la extensión del componente.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4bc6c0a8bb634706750810484963e56b6d6e0ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074610"
---
# <a name="ice41"></a>ICE41

ICE41 valida que las entradas de las tablas [Class](class-table.md) y [Extension](extension-table.md) hacen referencia a las entradas de la tabla [Component](component-table.md) que implementan el objeto de clase o la extensión del componente.

## <a name="result"></a>Resultado

ICE41 envía un error si hay una característica que no contiene el componente que implementa el objeto de clase o la extensión.

## <a name="example"></a>Ejemplo

ICE41 notifica los siguientes errores para el ejemplo mostrado.



| Error ICE41                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| La clase hace referencia a las características Feature2 y Component1, pero ese componente no está asociado a {00000000-0000-0000-0000-0000000000000} esa característica en la tabla FeatureComponents. | Hay una característica que no contiene el componente que implementa el objeto de clase. Esto significa que el instalador no instala el componente con la característica y que es posible que la publicidad no funcione según lo previsto. Para corregir este error, cambie la entrada de la columna Característica de la entrada de tabla Clase para hacer referencia a una característica que instala el componente que aparece en la columna Componente o cambie la característica y el componente asociados en la \_ [](class-table.md) \_ tabla [FeatureComponents](featurecomponents-table.md).<br/>          |
| La extensión .yip hace referencia a las características Feature1 y Component2, pero ese componente no está asociado a esa característica en la tabla FeatureComponents.                                | Hay una característica que no contiene el componente que implementa la extensión. Esto significa que el instalador no instala el componente con la característica y que es posible que la publicidad no funcione según lo previsto. Para corregir este error, cambie la entrada de la columna Característica de la entrada de la tabla Extensión para hacer referencia a una característica que instala el componente enumerado en la columna Componente o cambie la característica y el componente asociados en la \_ [](extension-table.md) \_ tabla [FeatureComponents](featurecomponents-table.md).<br/> |



 

[Tabla FeatureComponents](featurecomponents-table.md) (parcial)



| Característica\_ |
|-----------|
| Característica 1  |
| Característica 2  |



 

[Tabla de clases](class-table.md) (parcial)



| CLSID                                  | Componente\_ | Característica\_ |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | Componente1  | Característica 2  |



 

[Tabla de clases](class-table.md) (parcial)



| Extensión | Componente\_ | Característica\_ |
|-----------|-------------|-----------|
| .yip      | Componente 2  | Característica 1  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




