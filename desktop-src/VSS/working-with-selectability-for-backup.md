---
description: En la tabla siguiente se describen los cuatro tipos de componentes que pueden estar implicados en una operación de copia de seguridad.
ms.assetid: d94e015b-6735-4a88-9d24-b73f0b5f6542
title: Trabajar con selectability for Backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82081bb9cef51572afc2a8b5c08cf845ee22736dd8fdc20edf60fa0082ce8c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842319"
---
# <a name="working-with-selectability-for-backup"></a>Trabajar con selectability for Backup

En la tabla siguiente se describen los cuatro tipos de componentes que pueden estar implicados en una operación de copia de seguridad.



| Tipo de componente                                                                                                                                                                                                               | Descripción                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="Nonselectable-for-backup_components"></span><span id="nonselectable-for-backup_components"></span><span id="NONSELECTABLE-FOR-BACKUP_COMPONENTS"></span>Componentes no seleccionables para copia de seguridad<br/>             | No hay antecesores seleccionables para copia de seguridad en sus rutas de acceso lógicas.<br/>                              |
| <span id="Selectable-for-backup_components"></span><span id="selectable-for-backup_components"></span><span id="SELECTABLE-FOR-BACKUP_COMPONENTS"></span>Componentes seleccionables para copia de seguridad<br/>                         | No hay antecesores seleccionables para copia de seguridad en sus rutas de acceso lógicas.<br/>                              |
| <span id="Nonselectable-for-backup_subcomponents"></span><span id="nonselectable-for-backup_subcomponents"></span><span id="NONSELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Subcomponentes no seleccionables para copia de seguridad<br/> | Componentes no seleccionables para copia de seguridad con antecesores seleccionables para copia de seguridad en su ruta de acceso.<br/> |
| <span id="Selectable-for-backup_subcomponents"></span><span id="selectable-for-backup_subcomponents"></span><span id="SELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Subcomponentes seleccionables para copia de seguridad<br/>             | Componentes seleccionables para copia de seguridad con antecesores seleccionables para copia de seguridad en su ruta de acceso.<br/>    |



 

Además, cualquier componente seleccionable para copia de seguridad, independientemente de si tiene antecesores [](vssgloss-c.md) seleccionables para copia de seguridad o no, define un conjunto de componentes si otros componentes lo tienen como antecesor en sus rutas de acceso lógicas.

Las reglas que rigen la selección de componentes para la copia de seguridad se pueden resumir de la siguiente manera:

-   Cuando cualquier componente sin un antecesor seleccionable para copia de seguridad en su ruta de acceso lógica (independientemente de si [](vssgloss-e.md)el componente es seleccionable para copia de seguridad o no seleccionable para copia de seguridad) se incluye en una copia de seguridad, debe incluirse explícitamente. Esto significa que los metadatos de estos componentes se agregan al documento Componentes de copia de seguridad.

    Los solicitantes agregan explícitamente estos componentes mediante [**el método IVssBackupComponents::AddComponent.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)

-   Los subcomponentes no seleccionables para copia de seguridad siempre se [*incluyen implícitamente en*](vssgloss-i.md) la copia de seguridad. Esto significa que los metadatos de estos componentes no forman parte del documento componentes de copia de seguridad.
-   Los subcomponentes seleccionables para copia de seguridad se incluyen implícitamente si ese antecesor se incluye explícitamente en la copia de seguridad. En este caso, los metadatos de estos componentes no se agregan al documento Componentes de copia de seguridad. Si un subcomponente de copia de seguridad seleccionable implícitamente define un conjunto de componentes, los miembros de ese conjunto de componentes también se seleccionan implícitamente.
-   Los subcomponentes seleccionables para copia de seguridad cuyo antecesor selectable-for-backup no se incluye explícitamente en la copia de seguridad pueden incluirse explícitamente por el solicitante mediante el método [**IVssBackupComponents::AddComponent.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) A continuación, los metadatos del componente se agregarán al documento Componentes de copia de seguridad. Además, si un subcomponente seleccionable para copia de seguridad define un conjunto de componentes, los miembros de ese conjunto de componentes se incluyen implícitamente en la copia de seguridad.

El caso "MyWriter" que se describe en [Ruta](logical-pathing-of-components.md) de acceso lógica de componentes se puede usar como ejemplo para ilustrar la capacidad de selección de la copia de seguridad.



| Nombre de componente | Ruta de acceso lógica            | Seleccionable para copia de seguridad |
|----------------|-------------------------|-----------------------|
| "Ejecutables"  | ""                      | N                     |
| "ConfigFiles"  | "Ejecutables"           | N                     |
| "LicenseInfo"  | ""                      | Y                     |
| "Security"     | ""                      | Y                     |
| "UserInfo"     | "Security"              | N                     |
| "Certificados" | "Security"              | N                     |
| "writerData"   | ""                      | Y                     |
| "Set1"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set1"      | N                     |
| "Dec"          | "writerData \\ Set1"      | N                     |
| "Set2"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set2"      | N                     |
| "Dec"          | "writerData \\ Set2"      | N                     |
| "Consulta"        | "writerData \\ QueryLogs" | N                     |
| "Uso"        | "writerData"            | Y                     |
| "Jan"          | "writerData \\ Usage"     | N                     |
| "Dec"          | "writerData \\ Usage"     | N                     |



 

Siempre que se haga una copia de seguridad de "MyWriter", incluir explícitamente el componente "Executables" mediante el método [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) incluirá implícitamente el componente "ConfigFiles".

El componente "LicenseInfo" es un componente independiente seleccionable para copia de seguridad. Se puede seleccionar mediante el método [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) a discreción del solicitante, pero su selección no seleccionará ningún otro componente.

El componente seleccionable para copia de seguridad "Security" define un conjunto de componentes simple que contiene dos subcomponentes no seleccionables para copia de seguridad, "UserInfo" y "Certificates". Si "Security" se incluye explícitamente para la copia de seguridad, "UserInfo" y "Certificates" siempre se incluyen implícitamente también. No hay ninguna manera de incluir los subcomponentes "UserInfo" o "Certificates" en una operación de copia de seguridad a menos que se incluya "Security".

Si se selecciona el componente "writerData", se seleccionan implícitamente los componentes no seleccionables para copia de seguridad "Set1", "Set2" y "Query", así como el componente seleccionable para copia de seguridad "Usage". Cada uno de estos componentes tiene subcomponentes que se seleccionan implícitamente para la copia de seguridad. Ninguno de sus metadatos se agregará al documento componentes de copia de seguridad.

Si el componente "writerData" no está seleccionado, los componentes no seleccionables para copia de seguridad "Set1", "Set2" y "Query" no se incluyen para la copia de seguridad.

Sin embargo, los solicitantes pueden optar por incluir explícitamente el componente seleccionable para copia de seguridad "Usage". Los metadatos de este componente se agregarán al documento Componentes de copia de seguridad. Los subcomponentes "Jan" y "Dec" de "Usage" se agregarán implícitamente a la copia de seguridad, pero no tendrán su información agregada al documento componentes de copia de seguridad.

Si se incluye explícitamente un componente para la copia de seguridad, se creará una instancia [**de IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente en el documento componentes de copia de seguridad.

Un solicitante recuperará información sobre los componentes incluidos explícitamente de su documento de componentes de copia de seguridad examinando esos escritores (mediante [**IVssBackupComponents::GetWriterComponents) incluidos**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)en su documento y recuperando los objetos [**IVssComponent almacenados.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Como no estará presente la información del conjunto de archivos (especificación de archivo, ruta de acceso y marca de recursividad) de los componentes presentes en el documento componentes de copia de seguridad ni información sobre los componentes agregados implícitamente, los solicitantes tendrán que consultar los documentos de metadatos del escritor para obtener información completa sobre todos los componentes incluidos en el documento componentes de copia de seguridad.

 

 




