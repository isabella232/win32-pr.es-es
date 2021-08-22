---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: B (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f20bbe9f858066d7fca09a3f263aa618c79c4174664b9a4e0994c900fb81c75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998055"
---
# <a name="b-volume-shadow-copy-service"></a>B (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N O](vssgloss-n.md) [](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**Aplicaciones de nivel de back-end**
</dt> <dd>

Indica el punto en el que VSS notifica a un escritor una inmovilización. Los escritores que se inicializan como aplicaciones de nivel de back-end se notifican después de que los escritores se inicializaron como aplicaciones de nivel de front-end y antes de las inicializadas como aplicaciones de nivel de sistema. Consulte también [*aplicaciones de nivel de*](vssgloss-a.md)aplicación, aplicaciones de nivel de [*front-end,*](vssgloss-f.md) [*aplicaciones de nivel de sistema*](vssgloss-s.md)y [*escritor.*](vssgloss-w.md)

</dd> <dt>

<span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**Evento BackupComplete**
</dt> <dd>

Evento de VSS que indica que se ha completado una copia de seguridad de VSS. Este evento debe ir seguido de un evento BackupShutdown en funcionamiento normal. Vea también evento *BackupShutdown*.

</dd> <dt>

<span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Documento de componentes de copia de seguridad**
</dt> <dd>

Documento XML creado por un solicitante (mediante la interfaz **IVssBackupComponents)** durante la configuración de una operación de restauración o copia de seguridad. El documento Componentes de copias de seguridad contiene una lista de los componentes incluidos explícitamente, de uno o varios escritores, que participan en una operación de copia de seguridad o restauración. No contiene información de los componentes incluidos implícitamente. En cambio, un documento de metadatos de escritor solo contiene componentes de escritura que pueden participar en una copia de seguridad.

Un documento de componentes de copia de seguridad se puede guardar en el disco. Vea también [*inclusión explícita de componentes*](vssgloss-e.md), [*inclusión implícita de componentes*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**conjunto de copia de seguridad**
</dt> <dd>

Archivos de los que se va a realizar una copia de seguridad. Incluye los archivos seleccionados por inclusión en un componente, los indicados por instrucciones de inclusión de nivel de escritor, menos los archivos que se han incluido explícitamente.

</dd> <dt>

<span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**Evento BackupShutdown**
</dt> <dd>

Evento de VSS que indica que se ha cerrado una aplicación de copia de seguridad compatible. Normalmente, esto va precedido de un evento BackupComplete. Sin embargo, si una copia de seguridad finaliza inesperadamente, este evento se puede generar sin un evento BackupComplete anterior. Vea también evento *BackupComplete*.

</dd> <dt>

<span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**marca de copia de seguridad**
</dt> <dd>

Cadena que contiene información sobre cuándo se realizó una copia de seguridad. VSS no coloca ninguna restricción en el formato de esta cadena, salvo que es inteligible para todas las instancias de escritor de una clase determinada. Puede contener información de fecha y hora, números de secuencia lógicos o cualquier otra información que permita a un escritor de la misma clase determinar cuándo se ha hecho la última copia de seguridad.

</dd> </dl>

 

 



