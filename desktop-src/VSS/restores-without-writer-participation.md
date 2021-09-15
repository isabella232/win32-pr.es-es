---
description: La participación del escritor en una copia de seguridad de VSS está diseñada para permitir que las aplicaciones controlen qué y cómo se usarán sus datos de restauración.
ms.assetid: 076b2e6f-c2ca-4129-8827-1b18a655d634
title: Restauraciones sin participación del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89fd5ea855d2d91701d351e860bf966148be587
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474590"
---
# <a name="restores-without-writer-participation"></a>Restauraciones sin participación del escritor

La participación del escritor en una copia de seguridad de VSS está diseñada para permitir que las aplicaciones controlen qué y cómo se usarán sus datos de restauración.

En general, si un escritor está disponible en un sistema, nunca es aconsejable restaurar los datos a su ubicación original sin la participación del escritor. Esta restauración probablemente encontraría archivos de destino bloqueados y corre un riesgo significativo de dañar los datos.

Sin embargo, hay motivos por los que una aplicación de copia de seguridad podría querer o necesitar restaurar una copia de seguridad de VSS sin la participación del escritor:

-   Los datos se administran mediante aplicaciones que no son conscientes de VSS. Casi todos los sistemas tendrán algunas aplicaciones (editores de texto, lectores de correo electrónico, procesadores de texto, etc.) que no son conscientes de VSS. Estos datos no se pueden restaurar mediante la participación del escritor.

    Por lo general, este tipo de datos no es crítico para el sistema ni para el servicio, y restaurarlos no debería ser problemático o, al menos, no ser más problemático que durante una restauración convencional.

    Al igual que con los preparativos para restauraciones convencionales, si es posible, los operadores de restauración deben intentar suspender o finalizar dichas aplicaciones antes de iniciar una restauración de VSS.

-   Faltan vss writers. Esta situación puede ser bastante común al restaurar el estado de un sistema dañado. Una operación de copia de seguridad debe determinar si es conveniente restaurar los archivos para los escritores que faltan. Si la restauración es deseable, los archivos se pueden restaurar del mismo modo que una copia de seguridad convencional los restauraría.
-   Restauración privada de los datos de un escritor. Un solicitante puede optar por restaurar los datos de un escritor en ejecución en alguna ubicación privada sin notificar al escritor. Un ejemplo de esto podría ser la restauración de los datos del escritor para admitir la comparación sin conexión. En este tipo de situación, un solicitante [](vssgloss-n.md) no querrá usar la nueva ubicación de destino mientras realiza la restauración, porque no quiere que el escritor acceda a los datos.
-   Un sistema de escritura no quiere estar implicado durante la restauración. Un escritor indica esto pasando VSS WRE NEVER para el parámetro \_ \_ *writerRestore* de [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
-   Un sistema de escritura requiere un método de restauración personalizado. Un sistema de escritura indica que requiere una restauración personalizada pasando VSS RME CUSTOM para el parámetro de método \_ \_ de [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).  En este caso, este escritor no debe estar implicado en el proceso de restauración a menos que la documentación de restauración personalizada de ese escritor indique lo contrario.

Un solicitante implica a un escritor en el proceso de restauración especificando uno de los componentes de ese escritor en una llamada a [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore). Los datos de un escritor se pueden restaurar sin implicar al escritor simplemente sin especificar ninguno de los componentes de ese escritor en una llamada a **IVssBackupComponents::SetSelectedForRestore**. Si un escritor no espera ningún evento de restauración, la implicación de ese escritor en el proceso de restauración puede provocar errores falsos para ese escritor.

 

 



