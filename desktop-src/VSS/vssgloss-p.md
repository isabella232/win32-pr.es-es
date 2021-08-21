---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: P (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3dbcf3f9d4938e407b82c58482cabab08156c3b9fabac6c1770ec20d0a40394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121615"
---
# <a name="p-volume-shadow-copy-service"></a>P (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) H [I](vssgloss-h.md) [](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P P [Q R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**compatibilidad con archivos parciales**
</dt> <dd>

Capacidad para implementar operaciones de copia de seguridad mediante la modificación de subsecciones de los archivos implicados, en lugar de trabajar con todos los archivos. Vea también [*el destino dirigido.*](vssgloss-d.md)

</dd> <dt>

<span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**instantánea persistente**
</dt> <dd>

Instantánea que no se elimina automáticamente cuando el solicitante libera un objeto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) o cuando se reinicia el equipo. Consulte también [*auto-release shadow copy*](vssgloss-a.md), [*shadow copy*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plex**
</dt> <dd>

Un tipo especial de volumen de instantáneas que representa por completo y por completo un volumen de instantáneas sin necesidad de ninguno de los volúmenes originales. Esto también se conoce normalmente como reflejo dividido, pero en esta documentación se usa el término Plex.

</dd> <dt>

<span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**Evento PostRestore**
</dt> <dd>

Evento de VSS que indica que se ha completado una restauración de VSS.

</dd> <dt>

<span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**Evento PostSnapshot**
</dt> <dd>

Evento de VSS que indica que se ha completado una instantánea. Consulte también [*instantánea .*](vssgloss-s.md)

</dd> <dt>

<span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**Evento PrepareForBackup**
</dt> <dd>

Evento de VSS que indica que se va a realizar una operación de copia de seguridad.

</dd> <dt>

<span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**Evento PrepareForSnapshot**
</dt> <dd>

Evento de VSS que indica que los escritores deben tomar medidas para prepararse para una próxima operación de instantáneas. Consulte también [*instantánea .*](vssgloss-s.md)

</dd> <dt>

<span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**Evento PreRestore**
</dt> <dd>

Evento de VSS que indica que está a punto de realizarse una operación de restauración.

</dd> <dt>

<span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**Proveedor**
</dt> <dd>

Objeto de sistema operativo que intercepta y administra las solicitudes de E/S para crear y representar instantáneas de volumen en el sistema de archivos. Consulte también [*proveedor de hardware*](vssgloss-h.md), proveedor de [*software*](vssgloss-s.md).

</dd> </dl>

 

 



