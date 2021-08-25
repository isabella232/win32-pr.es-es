---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92843e9277709a1138bc51b403089c932387e1b282e349c7907fc4cde88e9de8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124485"
---
# <a name="s-volume-shadow-copy-service"></a>S (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) H [I](vssgloss-h.md) [](vssgloss-i.md) J K [L](vssgloss-l.md) M [N O](vssgloss-n.md) [](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selectability for backup (capacidad de selección de copia de seguridad)**
</dt> <dd>

Se dice que un componente se puede seleccionar para la copia de seguridad si su inclusión explícita en una operación de copia de seguridad es opcional. La capacidad de selección para la copia de seguridad está habilitada si el valor del **miembro bSelectable** de la estructura [**\_ COMPONENTINFO de VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) es **true.** No hay ningún valor predeterminado para la capacidad de selección de un componente para la copia de seguridad; un escritor siempre debe establecer este valor explícitamente.

Los escritores también usan la capacidad de selección de la restauración para organizar la participación de su componente en las operaciones de restauración.

Vea también *componente seleccionable, capacidad* de selección para *la restauración,* [*inclusión explícita de componentes,*](vssgloss-e.md) [*inclusión implícita de componentes*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**capacidad de selección para la restauración**
</dt> <dd>

Se dice que un componente se puede seleccionar para la restauración si se puede realizar una copia de seguridad implícitamente como parte de un conjunto de componentes y, después, restaurarlo individualmente sin el resto del conjunto de componentes. La capacidad de selección para la restauración está habilitada si el valor del miembro **bSelectableForRestore** de la estructura [**\_ COMPONENTINFO de VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) es **true.** De forma predeterminada, la capacidad de selección de un componente para la restauración es **false.** La capacidad de selección para la restauración solo tiene significado cuando no se ha agregado un componente al documento de copia de seguridad.

Vea también componente *seleccionable, capacidad* de selección para *copia de seguridad,* [*inclusión explícita de componentes,*](vssgloss-e.md) [*inclusión implícita de componentes*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**componente seleccionable**
</dt> <dd>

Se dice que un componente se puede seleccionar si su inclusión explícita en una operación de copia de seguridad o restauración es opcional.

La capacidad de selección de la copia de seguridad y la capacidad de selección para la restauración son independientes entre sí: es posible seleccionar un componente para ambas operaciones, para la restauración y no para la copia de seguridad, o para la copia de seguridad y no para la restauración.

Los escritores también usan la capacidad de selección para organizar sus componentes en grupos:

-   Los componentes no seleccionables sin antecesores seleccionables en sus rutas de acceso lógicas siempre deben incluirse explícitamente si se va a realizar una copia de seguridad de un sistema de escritura o restaurarlo.
-   Los componentes no seleccionables con antecesores seleccionables solo se incluirán en una copia de seguridad o restauración si se incluye al menos un antecesor seleccionable.
-   Los componentes seleccionables sin antecesores seleccionables solo se pueden incluir en una operación de copia de seguridad o restauración explícitamente.
-   Los componentes seleccionables con antecesores seleccionables se pueden incluir explícitamente en una operación de copia de seguridad o restauración, o se pueden incluir implícitamente si se incluye uno de sus antecesores seleccionables.

Vea también componentes [*, capacidad de*](vssgloss-c.md)selección para copia de *seguridad,* *capacidad de* selección para la restauración, [*inclusión explícita de componentes,*](vssgloss-e.md) [*inclusión implícita de componentes*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**Instantánea**
</dt> <dd>

Réplica a un momento dado de solo lectura del contenido de un volumen original. Cada instantánea está claveda por un GUID persistente. También se denomina instantánea de volumen. Consulte también *conjunto de instantáneas*.

</dd> <dt>

<span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Instantáneas para carpetas compartidas**
</dt> <dd>

Una característica de Windows que crea copias de seguridad ligeras y en línea de volúmenes mediante VSS. Los clientes pueden acceder a estas copias de seguridad a través del shell de Windows para ver las versiones anteriores de los archivos y deshacer errores sin necesidad de una restauración completa. Consulte también [*instantáneas accesibles para el cliente.*](vssgloss-c.md)

</dd> <dt>

<span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**conjunto de instantáneas**
</dt> <dd>

Colección de instantáneas de volumen creadas al mismo tiempo e identificadas por un valor común de identificador de conjunto de instantáneas (un GUID persistente). Este es el mecanismo que se usa para permitir que una operación de instantánea se pueda administrar entre volúmenes. Consulte también *instantánea.*

</dd> <dt>

<span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**proveedor de software**
</dt> <dd>

Proveedor que intercepta las solicitudes de E/S en el nivel de software entre el sistema de archivos y el administrador de volúmenes. Vea también [*el proveedor de hardware*](vssgloss-h.md), [*proveedor*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**Subcomponente**
</dt> <dd>

Cualquier componente que tenga una ruta de acceso lógica que contenga un componente primario seleccionable (para copia de seguridad o restauración). Los subcomponentes deben tener una ruta de acceso lógica con el formato {nombre del \_ componente} \\ {nombre del \_ subcomponente}. Si el antecesor seleccionable (para copia de seguridad o restauración) de un subcomponente se incluye explícitamente en una copia de seguridad o restauración, el subcomponente se incluye implícitamente en la operación. Los subcomponentes incluidos implícitamente no tienen sus datos incluidos en el documento componentes de copia de seguridad, independientemente de si se pueden seleccionar (para restauración o copia de seguridad) o no. Vea también el [*componente*](vssgloss-c.md), [*ruta de acceso lógica*](vssgloss-l.md).

</dd> <dt>

<span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**instantánea de superficie**
</dt> <dd>

Un volumen copiado en la sombra visible para el espacio de nombres de Mount Manager de un sistema, lo que significa que **FindFirstVolume** y **FindNextVolume** pueden encontrarlo y que se generan notificaciones de llegada y salida del volumen. Todas las instantáneas expuestas también son instantáneas expuestas. Sin embargo, no es necesario exponer una instantánea expuesta. Si una instantánea es transportable, no se puede abrir. Consulte también instantánea [*expuesta,*](vssgloss-e.md) [*instantánea transportable.*](vssgloss-t.md)

</dd> <dt>

<span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Protección de archivos del sistema**
</dt> <dd>

Vea [*Windows File Protection.*](vssgloss-w.md)

</dd> <dt>

<span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**aplicaciones de nivel de sistema**
</dt> <dd>

Indica el punto en el que VSS notifica a un escritor una inmovilización. Los escritores que se inicializan como aplicaciones de nivel de sistema se notifican después de que los escritores se inicialicen como aplicaciones de nivel de front-end o como aplicaciones de nivel de back-end. Consulte también [*aplicaciones de nivel de*](vssgloss-a.md)aplicación, aplicaciones de nivel de [*back-end*](vssgloss-b.md)y [*aplicaciones de nivel de front-end.*](vssgloss-f.md)

</dd> <dt>

<span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**proveedor del sistema**
</dt> <dd>

Proveedor preinstalado predeterminado proporcionado como parte de Windows.

</dd> <dt>

<span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Carpeta del volumen del sistema**
</dt> <dd>

Un directorio compartido que almacena las copias compartidas de los archivos públicos de un dominio, es decir, los archivos que se replican entre todos los controladores de dominio del dominio.

</dd> </dl>

 

 



