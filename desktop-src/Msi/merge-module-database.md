---
description: La base de datos de un módulo de combinación contiene todas las propiedades de instalación y la lógica de instalación del módulo.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Base de datos de módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361030"
---
# <a name="merge-module-database"></a>Base de datos de módulo de combinación

La base de datos de un módulo de combinación contiene todas las propiedades de instalación y la lógica de instalación del módulo. Básicamente es una base de [datos de instalador](installer-database.md) o un archivo. msi simplificado. Los archivos de base de datos del módulo de combinación estándar se indican mediante una extensión. msm. Para obtener una lista de todas las tablas de base de datos que pueden existir en los módulos de combinación, vea [Merge Module Database tables](merge-module-database-tables.md). Las tablas siguientes son necesarias en la base de datos de cada archivo. MSM:

[Componente](component-table.md)

[Directorio](directory-table.md)

[FeatureComponents](featurecomponents-table.md)

[Archivo](file-table.md)

[ModuleSignature](modulesignature-table.md)

[ModuleComponents](modulecomponents-table.md)

Tenga en cuenta que las tablas Component, Directory, FeatureComponents y File también están presentes en todos los archivos. msi. Una base de datos de módulo de combinación no contiene una [tabla de características](feature-table.md) , por lo que el archivo. MSM no se puede instalar por sí solo. Para instalar un módulo de combinación, primero debe combinarse mediante una herramienta de combinación en un archivo. msi.

La [tabla ModuleSignature](modulesignature-table.md) solo está presente en archivos. msi que se han combinado con al menos un archivo. msm. Si esta tabla está presente en un archivo. msi, contiene un registro para cada módulo de combinación que se ha combinado previamente en la base de datos de instalación.

Los módulos de combinación pueden contener tablas de secuencia módulo CRT opcionales. Estas tablas solo se producen en archivos. msm. Cuando los archivos. MSM se combinan en un archivo. msi, estas tablas modifican las [*tablas de secuencia*](s-gly.md) de acciones del archivo. msi.

Los módulos de combinación pueden contener tablas personalizadas. Estas tablas las utilizan las [acciones personalizadas](custom-actions.md) definidas en el módulo de combinación.

Los módulos de combinación raramente requieren tablas de interfaz de usuario. Estas tablas solo deben estar presentes en casos raros en los que el módulo de combinación requiere la intervención del usuario durante la instalación. Para obtener más información, vea [creación de interfaces de usuario en módulos de combinación](authoring-user-interfaces-in-merge-modules.md).

 

 



