---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26e7eaae-f540-47d1-99ec-6af0fd223039
title: D (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25af02bd43c5130fa7ce60ed08ec4ab822ff1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696455"
---
# <a name="d-volume-shadow-copy-service"></a>D (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) D [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_database_component"></span><span id="BASE.VSSGLOSS_DATABASE_COMPONENT"></span>**componente de base de datos**
</dt> <dd>

Grupo de archivos que utiliza una base de datos y que define un escritor que necesita ser administrado como una unidad durante las operaciones de copia de seguridad y restauración. Vea también [*componente*](vssgloss-c.md), [*componente de grupo de archivos*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_default_provider"></span><span id="BASE.VSSGLOSS_DEFAULT_PROVIDER"></span>**proveedor predeterminado**
</dt> <dd>

Vea [*proveedor del sistema*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_deleted_shadow_copy"></span><span id="BASE.VSSGLOSS_DELETED_SHADOW_COPY"></span>**instantánea eliminada**
</dt> <dd>

No se puede acceder a las instantáneas eliminadas en absoluto y no deben ser accesibles en ningún momento en el futuro.

</dd> <dt>

<span id="base.vssgloss_dependency"></span><span id="BASE.VSSGLOSS_DEPENDENCY"></span>**pendiente**
</dt> <dd>

Vea [*dependencia del componente*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_device_object"></span><span id="BASE.VSSGLOSS_DEVICE_OBJECT"></span>**objeto de dispositivo**
</dt> <dd>

Cadena que indica la "raíz" de un volumen de la instantánea. Se puede hacer referencia a los archivos y directorios de un volumen de copia sombra anteponiendo la cadena de objeto de dispositivo a una ruta de acceso correspondiente en el volumen original. Tal como se obtiene como el miembro **m \_ pwszSnapshotDeviceObject** de la estructura [**\_ \_ prop de instantáneas de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) , el objeto de dispositivo no tiene ninguna barra diagonal inversa (" \\ ").

</dd> <dt>

<span id="base.vssgloss_diff_area"></span><span id="BASE.VSSGLOSS_DIFF_AREA"></span>**área de diferencia**
</dt> <dd>

Ubicación en el volumen donde se almacenan los *datos diferenciales* . Esto también se conoce como espacio de almacenamiento de instantáneas.

</dd> <dt>

<span id="base.vssgloss_differenced_files"></span><span id="BASE.VSSGLOSS_DIFFERENCED_FILES"></span>**archivos diferenciados**
</dt> <dd>

Archivos implicados en una operación de copia de seguridad incremental o diferencial implementada mediante la actualización de archivos completos (en lugar de modificar las secciones de esos archivos mediante la compatibilidad con archivos parciales). Por ejemplo, si se va a implementar una copia de seguridad diferencial, todo un archivo (en lugar de simplemente la sección modificada) se copia en un medio de copia de seguridad, ese archivo es un archivo diferenciado. Vea también [*operaciones de copia de seguridad incremental*](vssgloss-i.md), *operaciones de copia de seguridad diferenciales*, [*compatibilidad con archivos parciales*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_differential_backup_operations"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_BACKUP_OPERATIONS"></span>**operaciones de copia de seguridad diferenciales**
</dt> <dd>

Operación de copia de seguridad o restauración realizada solo en archivos creados o modificados desde la última vez que se guardó la copia de seguridad completa. Vea también [*operaciones de copia de seguridad incremental*](vssgloss-i.md), [*compatibilidad con archivos parciales*](vssgloss-p.md)y *archivos diferenciados*.

</dd> <dt>

<span id="base.vssgloss_differential_data"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_DATA"></span>**datos diferenciales**
</dt> <dd>

Datos que se pueden aplicar a un volumen original para generar un volumen de instantánea. Esto también se conoce como datos de copia en escritura, pero en esta documentación se usa el término datos diferenciales.

</dd> <dt>

<span id="base.vssgloss_directed_targeting"></span><span id="BASE.VSSGLOSS_DIRECTED_TARGETING"></span>**destinatarios dirigidos**
</dt> <dd>

Modo de restauración por el que un escritor indica que, cuando se va a restaurar un archivo, se debe reasignar (el archivo de origen). El archivo se puede restaurar en una nueva ubicación de restauración y/o intervalos de sus datos restaurados a un desplazamiento diferente con la ubicación de restauración.

</dd> </dl>

 

 



