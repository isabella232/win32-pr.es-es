---
description: Los escritores pueden ajustar el rendimiento de varios tipos de copia de seguridad en el nivel de conjunto de archivos indicando a través de un tipo de copia de seguridad de especificación de archivo, indicado por una máscara de bits o OR bit a bit de los miembros de la enumeración VSS \_ FILE \_ SPEC BACKUP \_ \_ TYPE.
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Compatibilidad con esquemas de nivel de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473370"
---
# <a name="file-level-schema-support"></a>Compatibilidad con esquemas de nivel de archivo

Los escritores pueden ajustar el rendimiento de [](vssgloss-f.md) varios tipos de copia de seguridad en el nivel de conjunto de archivos indicando a través de un tipo de copia de seguridad de especificación de archivo, indicado por una máscara de bits o OR bit a bit de los miembros de la enumeración [**VSS \_ FILE SPEC \_ \_ BACKUP \_ TYPE.**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)

Para los tipos de copia de seguridad especificados, el sistema de escritura indica lo siguiente:

-   Si será necesario realizar una instantánea del volumen para realizar correctamente una copia de seguridad de un conjunto de archivos. Por ejemplo, si el escritor no abre exclusivamente los archivos de un conjunto de archivos y puede asegurarse de que es estable, no se necesita una instantánea.
-   Si el solicitante tiene que realizar la copia de seguridad de tal manera que, independientemente de la hora de última modificación u otros problemas, se restaurará la versión de los archivos actuales del conjunto de archivos en la copia de seguridad. Normalmente, esto significa que el conjunto de archivos se copia como parte de la copia de seguridad.

Los valores de [**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que indican el requisito de instantánea son:

-   VSS \_ FSBT \_ ALL \_ SNAPSHOT \_ REQUIRED
-   SE REQUIERE UNA \_ INSTANTÁNEA COMPLETA DE VSS FSBT \_ \_ \_
-   INSTANTÁNEA DIFERENCIAL \_ DE VSS FSBT \_ \_ \_ REQUERIDA
-   SE REQUIERE INSTANTÁNEA \_ INCREMENTAL DE VSS FSBT \_ \_ \_
-   SE REQUIERE UNA \_ INSTANTÁNEA DE REGISTRO DE VSS FSBT \_ \_ \_

Los valores de [**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que indican el requisito de hacer una copia de seguridad de un archivo son:

-   VSS \_ FSBT \_ ALL \_ BACKUP \_ REQUIRED
-   SE REQUIERE COPIA \_ DE SEGURIDAD COMPLETA DE VSS FSBT \_ \_ \_
-   SE REQUIERE COPIA \_ DE SEGURIDAD DIFERENCIAL DE VSS FSBT \_ \_ \_
-   SE REQUIERE COPIA \_ DE SEGURIDAD INCREMENTAL DE VSS FSBT \_ \_ \_
-   SE REQUIERE LA \_ COPIA DE SEGURIDAD DE REGISTROS DE VSS FSBT \_ \_ \_

De forma predeterminada, los conjuntos de archivos se etiquetan con un tipo de copia de seguridad de especificación de archivo de VSS \_ FSBT \_ ALL BACKUP REQUIRED \_ \_ \| VSS \_ FSBT \_ ALL SNAPSHOT REQUIRED, \_ \_ lo que significa que siempre se requiere una instantánea para controlar los archivos del conjunto de archivos y que los archivos se deben copiar en todos los tipos de copia de seguridad.

 

 



