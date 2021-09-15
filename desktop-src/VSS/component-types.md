---
description: Los componentes indican el tipo de datos que representan a través de un tipo.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Tipos de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473390"
---
# <a name="component-types"></a>Tipos de componentes

Los componentes indican el tipo de datos que representan a través de un tipo.

Actualmente, los tipos de componente [**(vea VSS \_ COMPONENT \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) están limitados a lo siguiente:

-   Componentes de base de datos
-   Grupos de archivos

Para obtener información de implementación sobre cómo establecer tipos de componentes, vea [Definición de componentes por escritores.](definition-of-components-by-writers.md)

Los escritores tienen un tipo de datos que indica su uso (vea [**VSS \_ SOURCE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), que puede ser el siguiente:

-   Una base de datos transaccional (por ejemplo, un SQL servidor)
-   Una base de datos no transaccional (por ejemplo, un cliente de hoja de cálculo)
-   Grupo de archivos (otro)

La especificación de un tipo de componente como base de datos permite una identificación más sencilla de su contenido, permite un control independiente de los archivos de registro y de datos (vea [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssExwriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) para obtener más información) y aplica un mayor poder en la selección de archivos al no permitir la selección de archivos recursiva o usar una ruta de acceso alternativa [*(vea*](vssgloss-a.md) [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) e [**IVssCreateWriterMetadata::AddDatabaseLogFiles).**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

Por otro lado, con un componente de grupo de archivos, a precio de no saber qué datos contiene, tiene mayor libertad sobre cómo se insertan los archivos, ya que puede usar la especificación recursiva y rutas de acceso alternativas.

En el futuro se pueden agregar tipos de componentes adicionales.

 

 



