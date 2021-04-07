---
description: Los escritores pueden ajustar el rendimiento de varios tipos de copia de seguridad en el nivel de conjunto de archivos indicando a través de un tipo de copia de seguridad de especificación de archivo, indicado por una máscara de bits o bit a bit o de los miembros de la \_ \_ enumeración de tipo de copia de seguridad de especificación de archivo de VSS \_ \_ .
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Compatibilidad con esquemas de nivel de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002949"
---
# <a name="file-level-schema-support"></a>Compatibilidad con esquemas de nivel de archivo

Los escritores pueden ajustar el rendimiento de varios tipos de copia de seguridad en el nivel de [*conjunto de archivos*](vssgloss-f.md) indicando a través de un tipo de copia de seguridad de especificación de archivo, indicado por una máscara de bits o bit a bit o de los miembros de la enumeración de tipo de [**\_ copia de \_ \_ seguridad \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) de especificación de archivo de VSS.

En el caso de los tipos de copia de seguridad especificados, el escritor indica lo siguiente:

-   Si será necesario crear una instantánea del volumen para realizar correctamente la copia de seguridad de un conjunto de archivos. Por ejemplo, si los archivos de un conjunto de archivos no están abiertos exclusivamente por el escritor y pueden asegurarse de que es estable, no se necesita una instantánea.
-   Si el solicitante tiene que realizar la copia de seguridad de forma que, independientemente de la hora de la última modificación u otros problemas, se restaurará la versión actual de los archivos del conjunto de archivos en la copia de seguridad. Normalmente, esto significa que el conjunto de archivos se copia como parte de la copia de seguridad.

Los valores del [**\_ tipo de \_ copia \_ de \_ seguridad de especificación de archivo de VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que indican el requisito de instantánea son:

-   VSS \_ FSBT \_ todas las \_ instantáneas \_ necesarias
-   se \_ \_ requiere una \_ instantánea \_ completa de FSBT de VSS
-   se \_ \_ requiere la \_ instantánea \_ diferencial FSBT de VSS
-   se \_ \_ requiere la instantánea incremental FSBT de VSS \_ \_
-   se \_ \_ requiere la \_ instantánea de registro FSBT de VSS \_

Los valores del [**\_ tipo de \_ copia \_ de \_ seguridad de especificación de archivo de VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que indican el requisito de hacer una copia de seguridad de un archivo son:

-   VSS \_ FSBT \_ todas las \_ copias de seguridad \_ necesarias
-   se \_ \_ requiere la \_ copia de seguridad completa de FSBT de VSS \_
-   se \_ \_ requiere la \_ copia de seguridad diferencial FSBT \_ de VSS
-   se \_ \_ requiere la copia de seguridad incremental FSBT de VSS \_ \_
-   se \_ \_ requiere la \_ copia de seguridad de registros FSBT \_ de VSS

De forma predeterminada, los conjuntos de archivos se etiquetan con un tipo de copia de seguridad de especificación de archivo de VSS \_ FSBT \_ All \_ backup \_ required \| VSS \_ FSBT \_ All \_ Snapshot \_ required, lo que significa que siempre se requiere una instantánea en el control de los archivos del conjunto de archivos y que los archivos deben copiarse en todos los tipos de copia de seguridad.

 

 



