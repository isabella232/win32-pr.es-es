---
description: En el procedimiento siguiente se describen los pasos generales para crear módulos de combinación.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Creación de módulos de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159029"
---
# <a name="authoring-merge-modules"></a>Creación de módulos de combinación

En el procedimiento siguiente se describen los pasos generales para crear módulos de combinación.

**Para crear un nuevo módulo de combinación**

1.  Obtenga una herramienta de software que pueda usar para editar la base de datos del módulo de mezcla.
2.  Obtenga una base de datos de módulo de combinación en blanco.
3.  Genere un [GUID](guid.md) para el módulo de combinación. Debe usar este GUID al crear las claves principales de las tablas de base de datos en el módulo de combinación.
4.  Agregue un registro a la [tabla Component para](component-table.md) cada componente entregado por la combinación. Se requiere una tabla De componentes en cada módulo de combinación. Tenga en cuenta que los módulos de combinación funcionan con componentes y no con características. Sin embargo, en algunos casos, una entrada de tabla de base de datos puede necesitar hacer referencia a una característica. Para obtener más información, vea [Hacer referencia a características en módulos de mezcla.](referencing-features-in-merge-modules.md)
5.  Agregue una [tabla Directory al](directory-table.md) módulo merge que especifique el diseño de los directorios que el módulo de combinación agrega a la base de datos de destino. Se requiere una tabla Directory en cada módulo de combinación.
6.  Importe una tabla [FeatureComponents en blanco en la](featurecomponents-table.md) base de datos del módulo merge. Esta tabla vacía proporciona una guía para la herramienta de combinación en los casos en los que el archivo .msi no contiene su propia tabla FeatureComponents.
7.  Recopile todos los archivos entregados por este módulo de combinación y cree el archivo de archivado [MergeModule.CABinet.](mergemodule-cabinet.md) Agregue el archivador al módulo merge como una secuencia dentro del archivo .msm.
8.  Agregue un registro a la tabla File para cada archivo almacenado en MergeModule.CABinet.
9.  Agregue la información necesaria para identificar el módulo de combinación en la [tabla ModuleSignature](modulesignature-table.md). Cada módulo de combinación requiere una tabla ModuleSignature.
10. Enumera los componentes del módulo de combinación en la [tabla ModuleComponents](modulecomponents-table.md). Cada módulo de combinación requiere una tabla ModuleComponents.
11. Agregue tablas de secuencia de módulo de mezcla al archivo .msm solo si el módulo de mezcla necesita modificar las tablas de secuencia de la base de datos de instalación de destino. [](s-gly.md)
12. Agregue una \_ tabla Validation al módulo merge. Un módulo de combinación requiere una \_ tabla De validación para pasar la validación.
13. Los módulos de combinación requieren una interfaz de usuario en raras ocasiones. No se recomienda incluir una interfaz de usuario con un módulo de combinación. En los casos en los que se requiere una interfaz de usuario, las tablas de interfaz de usuario se pueden combinar en .msi archivo igual que otras tablas.
14. Agregue información del Registro a las tablas del Registro adecuadas en la base de datos del módulo merge. Agregue información del Registro para bibliotecas de tipos, clases, extensiones y verbos en las tablas [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)o [MIME.](mime-table.md) Toda la información del Registro puede ir a la [tabla del Registro](registry-table.md). No se recomienda el uso de la tabla SelfReg.
15. Agregue la información de resumen al flujo [de información de resumen del módulo de mezcla](merge-module-summary-information-stream-reference.md).
16. Ejecute la validación en todos los módulos de combinación antes de intentar la instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener bases de datos de módulos de combinación en blanco](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[Obtener herramientas de creación de módulos de mezcla](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[Asignar nombres a claves principales en bases de datos de módulos de mezcla](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[Creación de tablas de componentes de módulo de mezcla](authoring-merge-module-component-tables.md)
</dt> <dt>

[Creación de tablas de directorios de módulos de mezcla](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Creación de características de módulo de mezclaComponentes Tablas](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[Generar archivos de archivador MergeModule.CABinet](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[Creación de tablas de archivos de módulo de mezcla](authoring-merge-module-file-tables.md)
</dt> <dt>

[Creación de tablas ModuleSignature](authoring-modulesignature-tables.md)
</dt> <dt>

[Creación de tablas moduleComponents](authoring-modulecomponents-tables.md)
</dt> <dt>

[Creación de tablas de secuencias de módulos de combinación](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[Validación de módulos de combinación](validating-merge-modules.md)
</dt> <dt>

[Creación de interfaces de usuario en módulos de combinación](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Creación de tablas del Registro de módulos de mezcla](authoring-merge-module-registry-tables.md)
</dt> <dt>

[Información de resumen del módulo de creación de mezcla Secuencias](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[Referencia de flujo de información de resumen del módulo de mezcla](merge-module-summary-information-stream-reference.md)
</dt> <dt>

Validación de módulos de combinación
</dt> <dt>

[Uso de módulos de combinación de 64 bits](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



