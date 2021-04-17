---
description: Los componentes indican el orden de los datos que representan a través de un tipo.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Tipos de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697790"
---
# <a name="component-types"></a>Tipos de componentes

Los componentes indican el orden de los datos que representan a través de un tipo.

Actualmente, los tipos de componentes (vea [**\_ \_ tipo de componente de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) se limitan a lo siguiente:

-   Componentes de base de datos
-   Grupos de archivos

Para obtener información sobre la implementación de la configuración [de los tipos de componentes, consulte definición de componentes por escritores](definition-of-components-by-writers.md).

Los escritores tienen un tipo de datos que indica su uso (consulte [**\_ \_ tipo de origen de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), que puede ser el siguiente:

-   Una base de datos transaccional (como un servidor SQL Server)
-   Una base de datos no transaccional (como un cliente de hoja de cálculo)
-   Grupo de archivos (otro)

La especificación de un tipo de componente como base de datos permite la identificación más fácil de su contenido, permite el control independiente de los archivos de registro y de datos (vea [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) y [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para obtener más información) y aplica mayor rigor en la selección de archivos al no permitir la selección de archivos recursivos o usar una [*ruta de acceso alternativa*](vssgloss-a.md) (consulte [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) y [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

Por otro lado, con un componente de grupo de archivos, con el precio de no saber qué datos contiene, tiene mayor libertad sobre cómo se insertan los archivos, ya que puede usar una especificación recursiva y rutas de acceso alternativas.

Se pueden agregar más tipos de componentes en el futuro.

 

 



