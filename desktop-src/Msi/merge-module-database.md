---
description: La base de datos de un módulo de mezcla contiene todas las propiedades de instalación y la lógica de instalación del módulo.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Base de datos de módulos de mezcla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb75614218e7464879f62ea1527245e36d65d1dc14f19a9b82a13a893997f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804607"
---
# <a name="merge-module-database"></a>Base de datos de módulos de mezcla

La base de datos de un módulo de mezcla contiene todas las propiedades de instalación y la lógica de instalación del módulo. Básicamente, es una base de [datos de instalador simplificada](installer-database.md) o .msi archivo. Los archivos de base de datos del módulo de mezcla estándar se indican mediante una extensión .msm. Para obtener una lista de todas las tablas de base de datos que pueden existir en los módulos de combinación, vea [Merge Module Database Tables](merge-module-database-tables.md). Las tablas siguientes son necesarias en la base de datos de cada archivo .msm:

[Componente](component-table.md)

[Directorio](directory-table.md)

[FeatureComponents](featurecomponents-table.md)

[Archivo](file-table.md)

[ModuleSignature](modulesignature-table.md)

[ModuleComponents](modulecomponents-table.md)

Tenga en cuenta que las tablas Component, Directory, FeatureComponents y File también están presentes en todos los .msi archivos. Una base de datos de módulos de mezcla no contiene una [tabla de características](feature-table.md) y, por tanto, el archivo .msm no se puede instalar por sí solo. Para instalar un módulo de combinación, primero debe combinarse mediante una herramienta de combinación en un archivo .msi combinación.

La [tabla ModuleSignature solo](modulesignature-table.md) está presente en .msi archivos que se han combinado con al menos un archivo .msm. Si esta tabla está presente en un archivo .msi, contiene un registro para cada módulo de mezcla que se ha combinado previamente en la base de datos de instalación.

Los módulos de combinación pueden contener tablas de secuencia MergeModule opcionales. Estas tablas solo se producen en archivos .msm. Cuando los archivos .msm se combinan en un archivo .msi, [](s-gly.md) estas tablas modifican las tablas de secuencia de acciones del .msi archivo.

Los módulos de combinación pueden contener tablas personalizadas. Estas tablas se usan mediante [acciones personalizadas](custom-actions.md) definidas en el módulo merge.

Los módulos de combinación rara vez requieren tablas de interfaz de usuario. Estas tablas solo deben estar presentes en casos excepcionales en los que el módulo de combinación requiere la entrada del usuario durante la instalación. Para obtener más información, [vea Creación de interfaces de usuario en módulos de mezcla.](authoring-user-interfaces-in-merge-modules.md)

 

 



