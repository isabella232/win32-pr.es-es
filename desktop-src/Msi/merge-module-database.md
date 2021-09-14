---
description: La base de datos de un módulo de combinación contiene todas las propiedades de instalación y la lógica de instalación del módulo.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Base de datos de módulos de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071895"
---
# <a name="merge-module-database"></a>Base de datos de módulos de mezcla

La base de datos de un módulo de combinación contiene todas las propiedades de instalación y la lógica de instalación del módulo. Básicamente, se trata de una base de [datos de instalador simplificada](installer-database.md) .msi archivo. Los archivos de base de datos del módulo de combinación estándar se indican mediante una extensión .msm. Para obtener una lista de todas las tablas de base de datos que pueden existir en los módulos de combinación, vea Combinar tablas de base [de datos de módulos](merge-module-database-tables.md). Las tablas siguientes son necesarias en la base de datos de cada archivo .msm:

[Componente](component-table.md)

[Directorio](directory-table.md)

[FeatureComponents](featurecomponents-table.md)

[Archivo](file-table.md)

[ModuleSignature](modulesignature-table.md)

[ModuleComponents](modulecomponents-table.md)

Tenga en cuenta que las tablas Component, Directory, FeatureComponents y File también están presentes en todos los .msi archivos. Una base de datos de módulos de mezcla no contiene una [tabla de características](feature-table.md) y, por tanto, el archivo .msm no se puede instalar por sí solo. Para instalar un módulo de combinación, primero debe combinarse mediante una herramienta de combinación en un archivo .msi combinación.

La [tabla ModuleSignature](modulesignature-table.md) solo está presente en .msi archivos que se han combinado con al menos un archivo .msm. Si esta tabla está presente en un archivo .msi, contiene un registro para cada módulo de combinación que se ha combinado previamente en la base de datos de instalación.

Los módulos de combinación pueden contener tablas de secuencia MergeModule opcionales. Estas tablas solo se producen en archivos .msm. Cuando los archivos .msm se combinan en un archivo .msi, [](s-gly.md) estas tablas modifican las tablas de secuencia de acción del .msi archivo.

Los módulos de combinación pueden contener tablas personalizadas. Estas tablas se usan mediante [acciones personalizadas](custom-actions.md) definidas en el módulo de combinación.

Los módulos de combinación rara vez requieren tablas de interfaz de usuario. Estas tablas solo deben estar presentes en casos excepcionales en los que el módulo de combinación requiere la entrada del usuario durante la instalación. Para obtener más información, vea [Creación de interfaces de usuario en módulos de mezcla.](authoring-user-interfaces-in-merge-modules.md)

 

 



