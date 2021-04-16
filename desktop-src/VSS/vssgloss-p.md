---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: P (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f018a19c1d00ff3c6530e7c45fbca2350df8fec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541731"
---
# <a name="p-volume-shadow-copy-service"></a>P (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) p Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**compatibilidad con archivos parciales**
</dt> <dd>

La capacidad de implementar las operaciones de copia de seguridad mediante la modificación de subsecciones de los archivos implicados, en lugar de trabajar con los archivos completos. Vea también [*destinos dirigidos*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**instantánea persistente**
</dt> <dd>

Una instantánea que no se elimina automáticamente cuando el solicitante libera un objeto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) o cuando se reinicia el equipo. Vea también instantánea [*de versión automática*](vssgloss-a.md), instantánea [*.*](vssgloss-s.md)

</dd> <dt>

<span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Complejos**
</dt> <dd>

Un tipo especial de volumen de instantánea que representa completamente y completamente un volumen de instantáneas sin necesidad de un volumen original. Esto también se conoce normalmente como un reflejo dividido, pero en esta documentación se usa el término Plex.

</dd> <dt>

<span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**Postrestore, evento**
</dt> <dd>

Un evento de VSS que indica que se ha completado una restauración de VSS.

</dd> <dt>

<span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**Evento postsnapshot**
</dt> <dd>

Un evento de VSS que indica que se ha completado una instantánea. Consulte también [*instantánea*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**Evento PrepareForBackup**
</dt> <dd>

Un evento de VSS que indica que está a punto de realizarse una operación de copia de seguridad.

</dd> <dt>

<span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**Evento PrepareForSnapshot**
</dt> <dd>

Un evento de VSS que indica que los escritores deben realizar pasos para preparar una próxima operación de instantánea. Consulte también [*instantánea*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**Evento de prerestauración**
</dt> <dd>

Un evento de VSS que indica que está a punto de realizarse una operación de restauración.

</dd> <dt>

<span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**presta**
</dt> <dd>

Objeto del sistema operativo que intercepta y administra las solicitudes de e/s para crear y representar instantáneas de volumen en el sistema de archivos. Vea también [*proveedor de hardware*](vssgloss-h.md), [*proveedor de software*](vssgloss-s.md).

</dd> </dl>

 

 



