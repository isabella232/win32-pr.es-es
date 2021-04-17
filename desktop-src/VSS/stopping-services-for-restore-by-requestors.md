---
description: Puede que sea necesario detener un servicio antes de y reiniciarlo después de una operación de restauración.
ms.assetid: 111d1281-ad83-49bc-868c-1106a0e25a2a
title: Detención de servicios para restauración por solicitante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548af25a4b4550d35a8e6fa4d4c0e791897b6e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697146"
---
# <a name="stopping-services-for-restore-by-requesters"></a>Detención de servicios para restauración por solicitante

Puede que sea necesario detener un servicio antes de y reiniciarlo después de una operación de restauración.

Normalmente, la detención e inicio de un servicio para admitir una restauración la realizaría un escritor al controlar el evento [*Prerestore*](vssgloss-p.md) (con [**CVssWriter:: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) y el evento [*postrestore*](vssgloss-p.md) (con [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)).

Sin embargo, puede haber casos en los que sea necesario que un solicitante detenga explícitamente un servicio en ejecución. Los escritores indican si este es el caso estableciendo el \_ \_ valor de VSS RME STOP \_ restore \_ Start o VSS \_ RME \_ restore \_ Stop \_ Start de la enumeración de [**\_ \_ enumeración RESTOREMETHOD de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) como argumento de método de restauración de una llamada al método [**IVssCreateWriterMetadata:: SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) y especificando el nombre del servicio que se va a detener.

Un solicitante obtiene información sobre el método restore y el nombre del servicio que se va a detener cuando se trabaja con metadatos del escritor mediante el método [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod) .

Es importante que el escritor, al especificar el nombre de un servicio que se va a detener, use el nombre público conocido de ese servicio. Un nombre ambiguo o inexacto puede dar lugar a que los solicitantes detengan el servicio equivocado o no puedan determinar qué servicio se debe detener.

Una vez finalizada la operación de restauración, los solicitantes deben reiniciar el servicio.

Debe tener cuidado al diseñar e implementar escritores que admitan servicios que los solicitantes deben detener y reiniciar. En concreto, estos escritores no deberían formar parte del servicio, es decir, el propio escritor no debe detenerse y reiniciarse en el transcurso de la operación de restauración.

Un escritor cuyo proceso se detiene tendrá una instancia de escritor diferente tras el reinicio. La nueva instancia del escritor no recibirá eventos de VSS destinados a la instancia original del escritor. En concreto, si se detiene el proceso de una instancia de escritor después de controlar un evento de prerestauración, la nueva instancia no recibirá el evento postrestore. Además, VSS generará un error que indica la pérdida de un escritor participante en la operación de restauración y [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) puede devolver un error.

 

 



