---
description: La participación del escritor en una copia de seguridad de VSS está diseñada para permitir que las aplicaciones controlen qué y cómo se van a usar los datos de restauración.
ms.assetid: 076b2e6f-c2ca-4129-8827-1b18a655d634
title: Restauraciones sin participación del escritor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89fd5ea855d2d91701d351e860bf966148be587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156109"
---
# <a name="restores-without-writer-participation"></a>Restauraciones sin participación del escritor

La participación del escritor en una copia de seguridad de VSS está diseñada para permitir que las aplicaciones controlen qué y cómo se van a usar los datos de restauración.

En general, si un escritor está disponible en un sistema, nunca es aconsejable restaurar los datos a su ubicación original sin la participación del escritor. Tal restauración podría encontrar archivos de destino bloqueados y corre un riesgo significativo de daños en los datos.

Sin embargo, hay motivos por los que una aplicación de copia de seguridad podría querer o necesitar restaurar una copia de seguridad de VSS sin la participación del escritor:

-   Las aplicaciones que no reconocen VSS administran los datos. Casi todos los sistemas tendrán algunas aplicaciones (editores de texto, lectores de correo, procesadores de textos, etc.) que no son conscientes de VSS. Estos datos no se pueden restaurar con la participación del escritor.

    Por lo general, este tipo de datos no es crítico para el sistema o el servicio, y la restauración no debe ser problemática o, al menos, no es problemático que durante una restauración convencional.

    Al igual que con los preparativos de las restauraciones convencionales, si es posible, los operadores de restauración deben intentar suspender o finalizar dichas aplicaciones antes de iniciar una restauración de VSS.

-   Escritores de VSS que faltan. Esta situación puede ser bastante común al restaurar el estado de un sistema dañado. Una operación de copia de seguridad debe determinar si es conveniente restaurar los archivos para los escritores que faltan. Si se desea la restauración, los archivos se pueden restaurar de la misma forma que una copia de seguridad convencional los restaurará.
-   Restauración privada de los datos de un escritor. Un solicitante puede optar por restaurar los datos de un escritor en ejecución en alguna ubicación privada sin notificar al escritor. Un ejemplo de esto podría ser la restauración de los datos del escritor para admitir la comparación sin conexión. En este tipo de situación, un solicitante no querrá usar la [*nueva ubicación de destino*](vssgloss-n.md) mientras realiza la restauración, ya que no quiere que el escritor tenga acceso a los datos.
-   Un escritor no desea estar implicado durante la restauración. Un escritor indica esto pasando VSS \_ WRE \_ nunca para el parámetro *writerRestore* de [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod).
-   Un escritor requiere un método de restauración personalizado. Un escritor indica que requiere una restauración personalizada pasando VSS \_ RME \_ personalizado para el parámetro de *método* de [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod). En este caso, este escritor no debe estar implicado en el proceso de restauración a menos que la documentación de restauración personalizada para ese escritor indique lo contrario.

Un solicitante implica un escritor en el proceso de restauración mediante la especificación de uno de los componentes de ese escritor en una llamada a [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore). Los datos de un escritor se pueden restaurar sin que intervenga el escritor simplemente si no se especifica ninguno de los componentes de ese escritor en una llamada a **IVssBackupComponents:: SetSelectedForRestore**. Si un escritor no espera ningún evento de restauración, en el proceso de restauración, el escritor puede provocar que se notifiquen falsos errores para ese escritor.

 

 



