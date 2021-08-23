---
description: Puede ser necesario que un servicio se detenga antes y se reinicie después de una operación de restauración.
ms.assetid: 111d1281-ad83-49bc-868c-1106a0e25a2a
title: Detener los servicios para restaurarlos los solicitantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa8051fc20c5ba1bd930da8c7da5c40829c07772572c2b1fb795250d34b8c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511625"
---
# <a name="stopping-services-for-restore-by-requesters"></a>Detener los servicios para restaurarlos los solicitantes

Puede ser necesario que un servicio se detenga antes y se reinicie después de una operación de restauración.

Normalmente, un escritor realiza la detención e inicio de un servicio para admitir una restauración al controlar el evento [*PreRestore*](vssgloss-p.md) (con [**CVssWriter::OnPreRestore)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)y el [*evento PostRestore*](vssgloss-p.md) (con [**CVssWriter::OnPostRestore).**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)

Sin embargo, puede haber casos en los que sea necesario que un solicitante detenga explícitamente un servicio en ejecución. Los escritores indican si este es el caso estableciendo el valor DE VSS RME STOP RESTORE START o VSS RME RESTORE STOP START de la enumeración ENUM DE VSS RESTOREMETHOD como argumento del método de restauración de una llamada al método \_ \_ \_ \_ \_ \_ \_ \_ [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) [**\_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) y especificando el nombre del servicio que se va a detener.

Un solicitante obtiene información sobre el método de restauración y el nombre del servicio que se va a detener al trabajar con metadatos del escritor mediante el método [**IVssExmethodMetadata::GetRestoreMethod.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)

Es importante que el escritor, al especificar el nombre de un servicio que se va a detener, use el nombre conocido públicamente correcto de ese servicio. Un nombre ambiguo o inexacto puede dar lugar a que los solicitantes detengan el servicio incorrecto o no puedan determinar qué servicio se debe detener.

Después de completar la operación de restauración, los solicitantes deben reiniciar el servicio.

Debe tener cuidado al diseñar e implementar escritores que admitan servicios que los solicitantes deben detener y reiniciar. En concreto, estos escritores no deberían formar parte del servicio, es decir, el propio escritor no debe detenerse y reiniciarse en el transcurso de la operación de restauración.

Un sistema de escritura cuyo proceso se detenga tendrá una instancia de escritor diferente al reiniciarse. La nueva instancia del sistema de escritura no recibirá eventos VSS destinados a la instancia original del escritor. En concreto, si el proceso de una instancia de escritor se detiene después de controlar un evento PreRestore, la nueva instancia no recibirá el evento PostRestore. Además, VSS generará un error que indica la pérdida de un escritor participante en la operación de restauración y [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) puede devolver un error.

 

 



