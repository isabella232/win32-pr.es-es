---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26e7eaae-f540-47d1-99ec-6af0fd223039
title: D (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3910a2fb09688e26b33b586f4558c05cb804688645486dfec751c9839fcff278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998035"
---
# <a name="d-volume-shadow-copy-service"></a>D (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) D [E](vssgloss-e.md) [F](vssgloss-f.md) G [H](vssgloss-g.md) [](vssgloss-h.md) [I](vssgloss-i.md) J K [L M](vssgloss-l.md) N [O](vssgloss-n.md) [](vssgloss-o.md) [P P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_database_component"></span><span id="BASE.VSSGLOSS_DATABASE_COMPONENT"></span>**componente de base de datos**
</dt> <dd>

Un grupo de archivos usados por una base de datos y definidos por un escritor como que deben controlarse como una unidad durante las operaciones de copia de seguridad y restauración. Vea también [*componente ,*](vssgloss-c.md)componente de grupo [*de archivos*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_default_provider"></span><span id="BASE.VSSGLOSS_DEFAULT_PROVIDER"></span>**proveedor predeterminado**
</dt> <dd>

Vea [*proveedor del sistema*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_deleted_shadow_copy"></span><span id="BASE.VSSGLOSS_DELETED_SHADOW_COPY"></span>**instantánea eliminada**
</dt> <dd>

Las instantáneas eliminadas no son accesibles en absoluto y no deben ser accesibles en ningún momento en el futuro.

</dd> <dt>

<span id="base.vssgloss_dependency"></span><span id="BASE.VSSGLOSS_DEPENDENCY"></span>**Dependencia**
</dt> <dd>

Consulte dependencia [*de componentes.*](vssgloss-c.md)

</dd> <dt>

<span id="base.vssgloss_device_object"></span><span id="BASE.VSSGLOSS_DEVICE_OBJECT"></span>**objeto device**
</dt> <dd>

Cadena que indica la "raíz" de un volumen sombreado. Se puede hacer referencia a los archivos y directorios de un volumen instantáneamente copiado anteponer la cadena de objeto de dispositivo a una ruta de acceso correspondiente en el volumen original. Como se obtiene como miembro **m \_ pwszSnapshotDeviceObject** de la estructura PROP de INSTANTÁNEA DE [**VSS, \_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) el objeto de dispositivo no tiene barra diagonal inversa (" \\ ").

</dd> <dt>

<span id="base.vssgloss_diff_area"></span><span id="BASE.VSSGLOSS_DIFF_AREA"></span>**área de diferencias**
</dt> <dd>

Ubicación en el volumen donde se almacenan *los datos* diferenciales. Esto también se conoce como espacio de almacenamiento de instantáneas.

</dd> <dt>

<span id="base.vssgloss_differenced_files"></span><span id="BASE.VSSGLOSS_DIFFERENCED_FILES"></span>**archivos con diferencias**
</dt> <dd>

Archivos implicados en una operación de copia de seguridad incremental o diferencial implementada mediante la actualización de archivos completos (en lugar de modificar secciones de esos archivos mediante compatibilidad parcial con archivos). Por ejemplo, si para implementar una copia de seguridad diferencial se copia un archivo completo (en lugar de solo la sección modificada) en un medio de copia de seguridad, ese archivo es un archivo con diferencias. Consulte también operaciones [*de copia de seguridad incrementales,*](vssgloss-i.md)operaciones *diferenciales de copia de* seguridad y compatibilidad con archivos [*parciales.*](vssgloss-p.md)

</dd> <dt>

<span id="base.vssgloss_differential_backup_operations"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_BACKUP_OPERATIONS"></span>**operaciones diferenciales de copia de seguridad**
</dt> <dd>

Una operación de copia de seguridad o restauración realizada solo en los archivos creados o modificados desde que se guardó la última copia de seguridad completa. Consulte también operaciones [*de copia de seguridad incrementales,*](vssgloss-i.md)compatibilidad con archivos [*parciales*](vssgloss-p.md)y *archivos con diferencias.*

</dd> <dt>

<span id="base.vssgloss_differential_data"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_DATA"></span>**datos diferenciales**
</dt> <dd>

Datos que se pueden aplicar a un volumen original para generar un volumen de instantáneas. Esto también se conoce normalmente como datos de copia en escritura, pero en esta documentación se usa el término datos diferenciales.

</dd> <dt>

<span id="base.vssgloss_directed_targeting"></span><span id="BASE.VSSGLOSS_DIRECTED_TARGETING"></span>**destino dirigido**
</dt> <dd>

Modo de restauración por el que un escritor indica que, cuando se va a restaurar un archivo, se debe volver a crear (el archivo de origen). El archivo se puede restaurar en una nueva ubicación de restauración o en intervalos de sus datos restaurados en un desplazamiento diferente con la ubicación de restauración.

</dd> </dl>

 

 



