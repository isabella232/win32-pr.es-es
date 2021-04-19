---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5979d30f0b88762a2d022a89063ee44bd91a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696448"
---
# <a name="s-volume-shadow-copy-service"></a>S (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) s [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selección de copia de seguridad**
</dt> <dd>

Se dice que un componente se puede seleccionar para la copia de seguridad si su inclusión explícita en una operación de copia de seguridad es opcional. La selección de la opción de copia de seguridad está habilitada si el valor del miembro **bSelectable** de la estructura [**\_ COMPONENTINFO de VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) es **true**. No hay ningún valor predeterminado para la selección de un componente para la copia de seguridad; un escritor siempre debe establecer este valor explícitamente.

Los escritores también usan la selección de la restauración para organizar la participación de sus componentes en las operaciones de restauración.

Vea también *componente seleccionable*, *selección de restauración*, [*inclusión explícita de componentes*](vssgloss-e.md), [*inclusión implícita de componentes*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selección de restauración**
</dt> <dd>

Se dice que un componente se puede seleccionar para la restauración si se puede realizar una copia de seguridad de forma implícita como parte de un conjunto de componentes y, posteriormente, se restaura de forma individual sin el resto del conjunto de componentes. La selección de la restauración está habilitada si el valor del miembro **bSelectableForRestore** de la estructura [**\_ COMPONENTINFO de VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) es **true**. De forma predeterminada, la selección de un componente para la restauración es **falsa**. La selección de la restauración solo tiene significado cuando no se ha agregado un componente al documento de copia de seguridad.

Vea también *componente seleccionable*, *selección de copia de seguridad*, [*inclusión explícita de componentes*](vssgloss-e.md), [*inclusión implícita de componentes*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**componente seleccionable**
</dt> <dd>

Se dice que un componente se puede seleccionar si su inclusión explícita en una operación de copia de seguridad o restauración es opcional.

La selección de la copia de seguridad y la selección de la restauración son independientes entre sí, ya que un componente puede seleccionarse para ambas operaciones, para restaurar y no para copias de seguridad, o para realizar copias de seguridad y no restaurar.

Los escritores también usan la selección para organizar sus componentes en grupos:

-   Siempre se deben incluir explícitamente los componentes no seleccionables sin antecesores seleccionables en sus rutas de acceso lógicas si se va a realizar la copia de seguridad o la restauración de un escritor.
-   Los componentes no seleccionables con antecesores seleccionables solo se incluirán en una copia de seguridad o restauración si se incluye al menos un antecesor seleccionable.
-   Los componentes seleccionables sin antecesores seleccionables solo se pueden incluir en una operación de copia de seguridad o restauración explícitamente.
-   Los componentes seleccionables con antecesores seleccionables se pueden incluir explícitamente en una operación de copia de seguridad o restauración, o se pueden incluir implícitamente si se incluye uno de sus antecesores seleccionables.

Vea también [*componentes*](vssgloss-c.md), *selección de copia de seguridad*, *la selección de la restauración*, [*inclusión explícita de componentes*](vssgloss-e.md), [*inclusión implícita de componentes*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**instantánea**
</dt> <dd>

Réplica en un momento dado de solo lectura del contenido de un volumen original. Cada instantánea está ordenada por un GUID persistente. También se denomina instantánea de volumen. Vea también *conjunto de instantáneas*.

</dd> <dt>

<span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Instantáneas para carpetas compartidas**
</dt> <dd>

Característica de Windows que crea copias de seguridad ligeras en línea de volúmenes con VSS. Los clientes pueden tener acceso a estas copias de seguridad a través del shell de Windows para ver las versiones anteriores de los archivos y deshacer los errores sin necesidad de una restauración completa. Vea también [*instantánea accesible del cliente*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**conjunto de instantáneas**
</dt> <dd>

Colección de instantáneas de volumen creadas al mismo tiempo e identificadas por un valor común de identificador de conjunto de instantáneas (GUID persistente). Este es el mecanismo que se usa para permitir la administración de una operación de instantáneas en los volúmenes. Consulte también *instantánea*.

</dd> <dt>

<span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**proveedor de software**
</dt> <dd>

Proveedor que intercepta las solicitudes de e/s en el nivel de software entre el sistema de archivos y el administrador de volúmenes. Vea también [*proveedor de hardware*](vssgloss-h.md), [*proveedor*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**subcomponente**
</dt> <dd>

Cualquier componente que tenga una ruta de acceso lógica que contenga un componente primario seleccionable (para copia de seguridad o restauración). Los subcomponentes deben tener una ruta de acceso lógica con la forma {nombre de componente \_ } \\ {nombre de subcomponente \_ }. Si el antecesor seleccionable de un subcomponente (para copia de seguridad o restauración) se incluye explícitamente en una copia de seguridad o restauración, el subcomponente se incluye implícitamente en la operación. Los subcomponentes incluidos implícitamente no tienen sus datos incluidos en el documento componentes de copia de seguridad, independientemente de si son seleccionables (para restauración o copia de seguridad) o no. Vea también [*componente*](vssgloss-c.md), [*ruta de acceso lógica*](vssgloss-l.md).

</dd> <dt>

<span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**instantáneas superficiales**
</dt> <dd>

Un volumen de copia sombra visible para el espacio de nombres del administrador de montaje de un sistema, lo que significa que **FindFirstVolume** y **FindNextVolume** pueden encontrarlo y que se generan notificaciones de llegada y salida de volumen. Todas las instantáneas expuestas también son instantáneas superficiales. Sin embargo, no es necesario exponer una instantánea superficial. Si una instantánea es transportable, no se puede mostrar. Vea también instantáneas [*expuestas*](vssgloss-e.md), instantáneas [*transportables*](vssgloss-t.md).

</dd> <dt>

<span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Protección de archivos del sistema**
</dt> <dd>

Consulte [*protección de archivos de Windows*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**aplicaciones de nivel de sistema**
</dt> <dd>

Indica el punto en el que VSS notifica a un escritor de una inmovilización. Los escritores que se inicializan como aplicaciones de nivel de sistema se notifican después de que los escritores se inicialicen como aplicaciones de nivel de front-end o como aplicaciones de nivel de back-end. Vea también [*nivel de aplicación*](vssgloss-a.md), [*aplicaciones de nivel de back-end*](vssgloss-b.md), [*aplicaciones de nivel de front-end*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**proveedor del sistema**
</dt> <dd>

El proveedor preinstalado predeterminado proporcionado como parte de Windows.

</dd> <dt>

<span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Carpeta de volumen del sistema**
</dt> <dd>

Directorio compartido que almacena las copias compartidas de los archivos públicos de un dominio, es decir, los archivos que se replican entre todos los controladores de dominio del dominio.

</dd> </dl>

 

 



