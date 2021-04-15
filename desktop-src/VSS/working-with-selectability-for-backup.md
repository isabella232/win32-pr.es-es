---
description: En la tabla siguiente se describen los cuatro tipos de componentes que pueden estar implicados en una operación de copia de seguridad.
ms.assetid: d94e015b-6735-4a88-9d24-b73f0b5f6542
title: Trabajar con la selección para la copia de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4bd20bd0c9139f8ed1c9f56cc8f499f1b6aaf14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497512"
---
# <a name="working-with-selectability-for-backup"></a>Trabajar con la selección para la copia de seguridad

En la tabla siguiente se describen los cuatro tipos de componentes que pueden estar implicados en una operación de copia de seguridad.



| Tipo de componente                                                                                                                                                                                                               | Descripción                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="Nonselectable-for-backup_components"></span><span id="nonselectable-for-backup_components"></span><span id="NONSELECTABLE-FOR-BACKUP_COMPONENTS"></span>Componentes no seleccionables para copia de seguridad<br/>             | No hay antecesores seleccionables para la copia de seguridad en sus rutas de acceso lógicas.<br/>                              |
| <span id="Selectable-for-backup_components"></span><span id="selectable-for-backup_components"></span><span id="SELECTABLE-FOR-BACKUP_COMPONENTS"></span>Componentes seleccionables para copia de seguridad<br/>                         | No hay antecesores seleccionables para la copia de seguridad en sus rutas de acceso lógicas.<br/>                              |
| <span id="Nonselectable-for-backup_subcomponents"></span><span id="nonselectable-for-backup_subcomponents"></span><span id="NONSELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Subcomponentes no seleccionables para la copia de seguridad<br/> | Componentes no seleccionables para la copia de seguridad con antecesores seleccionables para la copia de seguridad en su ruta de acceso.<br/> |
| <span id="Selectable-for-backup_subcomponents"></span><span id="selectable-for-backup_subcomponents"></span><span id="SELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Subcomponentes Selectable-for-Backup<br/>             | Componentes seleccionables para copia de seguridad con antecesores seleccionables para la copia de seguridad en su ruta de acceso.<br/>    |



 

Además, cualquier componente seleccionable para copia de seguridad, independientemente de si tiene antecesores seleccionables para la copia de seguridad o no, define un [*conjunto de componentes*](vssgloss-c.md) si otros componentes lo tienen como antecesor en sus rutas de acceso lógicas.

Las reglas que rigen la selección de componentes para la copia de seguridad se pueden resumir de la manera siguiente:

-   Cuando se incluye en una copia de seguridad cualquier componente sin un antecesor seleccionable para la copia de seguridad en su ruta de acceso lógica: Si el componente es seleccionable por copia de seguridad o no seleccionable-for-Backup, se debe [*incluir explícitamente*](vssgloss-e.md). Esto significa que los metadatos de estos componentes se agregan al documento componentes de copia de seguridad.

    Los solicitantes agregan estos componentes explícitamente mediante el método [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) .

-   Los subcomponentes no seleccionables para la copia de seguridad siempre se [*incluyen implícitamente*](vssgloss-i.md) en la copia de seguridad. Esto significa que los metadatos de estos componentes no forman parte del documento componentes de copia de seguridad.
-   Los subcomponentes Selectable-for-Backup se incluyen implícitamente si ese antecesor se incluye explícitamente en la copia de seguridad. En este caso, los metadatos de estos componentes no se agregan al documento componentes de copia de seguridad. Si un subcomponente que se puede seleccionar de forma implícita para realizar una copia de seguridad define un conjunto de componentes, los miembros de ese conjunto de componentes también se seleccionan implícitamente.
-   Los subcomponentes Selectable-for-Backup cuyo antecesor Selectable for Backup no se incluye explícitamente en la copia de seguridad todavía se pueden incluir explícitamente en el solicitante mediante el método [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) . Los metadatos del componente se agregarán entonces al documento componentes de copia de seguridad. Además, si un subcomponente Selectable-for-Backup define un conjunto de componentes, los miembros de ese conjunto de componentes se incluyen de forma implícita en la copia de seguridad.

El caso "alwriter" descrito en las [acciones lógicas de los componentes](logical-pathing-of-components.md) se puede usar como ejemplo para ilustrar la posibilidad de seleccionar la copia de seguridad.



| Nombre de componente | Ruta de acceso lógica            | Seleccionable para copia de seguridad |
|----------------|-------------------------|-----------------------|
| Aplicaciones  | ""                      | N                     |
| "ConfigFiles"  | Aplicaciones           | N                     |
| "LicenseInfo"  | ""                      | Y                     |
| "Security"     | ""                      | Y                     |
| UserInfo     | "Security"              | N                     |
| Firma | "Security"              | N                     |
| "writerData"   | ""                      | Y                     |
| Set1         | "writerData"            | N                     |
| Bernardo          | "writerData \\ Set1"      | N                     |
| Dec          | "writerData \\ Set1"      | N                     |
| Set2         | "writerData"            | N                     |
| Bernardo          | "writerData \\ Set2"      | N                     |
| Dec          | "writerData \\ Set2"      | N                     |
| Misma        | "writerData \\ QueryLogs" | N                     |
| Uso        | "writerData"            | Y                     |
| Bernardo          | "uso de writerData \\ "     | N                     |
| Dec          | "uso de writerData \\ "     | N                     |



 

Siempre que se realiza una copia de seguridad de "alwriters", si se incluye explícitamente el componente "ejecutables" con el método [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) , se incluirá implícitamente el componente "ConfigFiles".

El componente "LicenseInfo" es un componente independiente seleccionable para la copia de seguridad. Se puede seleccionar con el método [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) a discreción del solicitante, pero su selección no seleccionará ningún otro componente.

El componente Selectable-for-Backup "Security" define un conjunto de componentes sencillo que contiene dos subcomponentes no seleccionables para la copia de seguridad, "UserInfo" y "Certificates". Si se incluye "Security" explícitamente para la copia de seguridad, "UserInfo" y "Certificates" siempre se incluyen implícitamente. No hay ninguna manera de incluir los subcomponentes "UserInfo" o "Certificates" en una operación de copia de seguridad a menos que se incluya "Security".

Si se selecciona el componente "writerData", los componentes no seleccionables para la copia de seguridad "Set1", "Set2" y "Query", así como el componente Selectable-for-Backup "Usage", se seleccionan implícitamente. Cada uno de estos componentes tiene subcomponentes que se seleccionan implícitamente para la copia de seguridad. Ninguno de sus metadatos se agregará al documento componentes de copia de seguridad.

Si el componente "writerData" no está seleccionado, los componentes no seleccionables para la copia de seguridad "Set1", "Set2" y "Query" no se incluyen en la copia de seguridad.

Sin embargo, los solicitantes pueden optar por incluir explícitamente el elemento seleccionable para el componente de copia de seguridad "Usage". Los metadatos de este componente se agregarán al documento componentes de copia de seguridad. Los subcomponentes de "uso" "ene" y "Dec" se agregarán implícitamente a la copia de seguridad, pero no se agregará su información al documento componentes de copia de seguridad.

Al incluir explícitamente un componente para la copia de seguridad, se creará una instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente en el documento componentes de copia de seguridad.

Un solicitante recuperará información sobre los componentes incluidos explícitamente de su documento de componentes de copia de seguridad examinando esos escritores (mediante [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)) incluidos en su documento y recuperando los objetos [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) almacenados.

Como la información del conjunto de archivos (especificación de archivo, ruta de acceso y marca de recursividad) de los componentes presentes en el documento de componentes de copia de seguridad, o bien la información sobre los componentes agregados implícitamente estará presente, los solicitantes tendrán que consultar los documentos de metadatos del escritor para obtener información completa sobre todos los componentes incluidos en el documento componentes de copia de seguridad

 

 




