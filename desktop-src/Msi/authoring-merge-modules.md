---
description: En el procedimiento siguiente se describen los pasos generales para crear módulos de combinación.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Crear módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276517"
---
# <a name="authoring-merge-modules"></a>Crear módulos de combinación

En el procedimiento siguiente se describen los pasos generales para crear módulos de combinación.

**Para crear un nuevo módulo de combinación**

1.  Obtenga una herramienta de software que puede utilizar para editar la base de datos del módulo de fusión mediante combinación.
2.  Obtener una base de datos de módulo de mezcla en blanco.
3.  Genere un [GUID](guid.md) para el módulo de combinación. Debe usar este GUID al crear las claves principales de las tablas de base de datos en el módulo de combinación.
4.  Agregue un registro a la [tabla de componentes](component-table.md) para cada componente entregado por la combinación. En cada módulo de combinación se requiere una tabla de componentes. Tenga en cuenta que los módulos de combinación operan con componentes y no con características. Sin embargo, en algunos casos, es posible que una entrada de la tabla de base de datos tenga que hacer referencia a una característica. Para obtener más información, vea [hacer referencia a características en módulos de combinación](referencing-features-in-merge-modules.md).
5.  Agregue una [tabla de directorio](directory-table.md) al módulo de combinación que especifique el diseño de los directorios que el módulo de combinación agrega a la base de datos de destino. Se requiere una tabla de directorio en cada módulo de combinación.
6.  Importe una [tabla FeatureComponents](featurecomponents-table.md) en blanco en la base de datos del módulo de fusión mediante combinación. Esta tabla vacía proporciona una guía para la herramienta de combinación en los casos en los que el archivo. msi no contiene su propia tabla FeatureComponents.
7.  Recopile todos los archivos entregados por este módulo de combinación y cree el archivo. cab de [MergeModule.CABinet](mergemodule-cabinet.md) . Agregue el archivo. cab al módulo de combinación como una secuencia dentro del archivo. msm.
8.  Agregue un registro a la tabla de archivos para cada archivo almacenado en MergeModule.CABinet.
9.  Agregue la información necesaria para identificar el módulo de combinación en la [tabla ModuleSignature](modulesignature-table.md). Cada módulo de combinación requiere una tabla ModuleSignature.
10. Enumere los componentes del módulo de combinación en la [tabla ModuleComponents](modulecomponents-table.md). Cada módulo de combinación requiere una tabla ModuleComponents.
11. Agregue tablas de secuencia de módulo de combinación al archivo. MSM solo si el módulo de combinación debe modificar las [*tablas de secuencia*](s-gly.md) de la base de datos de instalación de destino.
12. Agregue una \_ tabla de validación al módulo de combinación. Un módulo de combinación requiere una \_ tabla de validación para pasar la validación.
13. Los módulos de combinación requieren una interfaz de usuario en solo casos raros. No se recomienda incluir una interfaz de usuario con un módulo de combinación. En los casos en los que se requiere una interfaz de usuario, las tablas de la interfaz de usuario se pueden combinar en el archivo. msi de la misma forma que otras tablas.
14. Agregue información del registro a las tablas del registro adecuadas en la base de datos del módulo de mezcla. Agregue información del registro para bibliotecas de tipos, clases, extensiones y verbos a las tablas [typelib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)o [MIME](mime-table.md) . Toda la demás información del registro puede incluirse en la [tabla del registro](registry-table.md). No se recomienda el uso de la tabla SelfReg.
15. Agregue la información de resumen al [flujo de información de resumen del módulo de combinación](merge-module-summary-information-stream-reference.md).
16. Ejecute la validación en todos los módulos de combinación antes de intentar instalar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener las bases de datos del módulo de combinación en blanco](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[Obtener herramientas de creación de módulos de fusión mediante combinación](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[Asignar nombres a las claves principales de las bases de datos de módulo de combinación](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[Crear tablas de componentes de módulo de combinación](authoring-merge-module-component-tables.md)
</dt> <dt>

[Crear tablas del directorio del módulo de combinación](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Crear tablas FeatureComponents de módulo de combinación](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[Generación de archivos. cab de MergeModule.CABinet](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[Crear tablas de archivos de módulo de combinación](authoring-merge-module-file-tables.md)
</dt> <dt>

[Creación de tablas ModuleSignature](authoring-modulesignature-tables.md)
</dt> <dt>

[Creación de tablas ModuleComponents](authoring-modulecomponents-tables.md)
</dt> <dt>

[Crear tablas de secuencia de módulo de combinación](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[Validar módulos de combinación](validating-merge-modules.md)
</dt> <dt>

[Crear interfaces de usuario en módulos de combinación](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Crear tablas del registro del módulo de combinación](authoring-merge-module-registry-tables.md)
</dt> <dt>

[Crear secuencias de información de resumen del módulo de combinación](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[Referencia de flujo de información de resumen del módulo de combinación](merge-module-summary-information-stream-reference.md)
</dt> <dt>

Validar módulos de combinación
</dt> <dt>

[Usar módulos de combinación de 64 bits](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



