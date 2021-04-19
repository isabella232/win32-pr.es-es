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
# <a name="s-volume-shadow-copy-service"></a><span data-ttu-id="e7eb2-103">S (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="e7eb2-103">S (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="e7eb2-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) s [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="e7eb2-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="e7eb2-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selección de copia de seguridad**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selectability for backup**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-106">Se dice que un componente se puede seleccionar para la copia de seguridad si su inclusión explícita en una operación de copia de seguridad es opcional.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-106">A component is said to be selectable for backup if its explicit inclusion in a backup operation is optional.</span></span> <span data-ttu-id="e7eb2-107">La selección de la opción de copia de seguridad está habilitada si el valor del miembro **bSelectable** de la estructura [**\_ COMPONENTINFO de VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) es **true**.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-107">Selectability for backup is enabled if the value of the **bSelectable** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="e7eb2-108">No hay ningún valor predeterminado para la selección de un componente para la copia de seguridad; un escritor siempre debe establecer este valor explícitamente.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-108">There is no default value for a component's selectability for backup; a writer must always set this value explicitly.</span></span>

<span data-ttu-id="e7eb2-109">Los escritores también usan la selección de la restauración para organizar la participación de sus componentes en las operaciones de restauración.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-109">Writers also use selectability for restore to organize their component's participation in restore operations.</span></span>

<span data-ttu-id="e7eb2-110">Vea también *componente seleccionable*, *selección de restauración*, [*inclusión explícita de componentes*](vssgloss-e.md), [*inclusión implícita de componentes*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="e7eb2-110">See also *selectable component*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selección de restauración**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selectability for restore**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-112">Se dice que un componente se puede seleccionar para la restauración si se puede realizar una copia de seguridad de forma implícita como parte de un conjunto de componentes y, posteriormente, se restaura de forma individual sin el resto del conjunto de componentes.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-112">A component is said to be selectable for restore if it can be implicitly backed up as part of a component set, and then later individually restored without the rest of the component set.</span></span> <span data-ttu-id="e7eb2-113">La selección de la restauración está habilitada si el valor del miembro **bSelectableForRestore** de la estructura [**\_ COMPONENTINFO de VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) es **true**.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-113">Selectability for restore is enabled if the value of the **bSelectableForRestore** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="e7eb2-114">De forma predeterminada, la selección de un componente para la restauración es **falsa**.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-114">By default, a component's selectability for restore is **false**.</span></span> <span data-ttu-id="e7eb2-115">La selección de la restauración solo tiene significado cuando no se ha agregado un componente al documento de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-115">Selectability for restore has meaning only when a component has not been added to the backup document.</span></span>

<span data-ttu-id="e7eb2-116">Vea también *componente seleccionable*, *selección de copia de seguridad*, [*inclusión explícita de componentes*](vssgloss-e.md), [*inclusión implícita de componentes*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="e7eb2-116">See also *selectable component*, *selectability for backup*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**componente seleccionable**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**selectable component**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-118">Se dice que un componente se puede seleccionar si su inclusión explícita en una operación de copia de seguridad o restauración es opcional.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-118">A component is said to be selectable if its explicit inclusion in a backup or restore operation is optional.</span></span>

<span data-ttu-id="e7eb2-119">La selección de la copia de seguridad y la selección de la restauración son independientes entre sí, ya que un componente puede seleccionarse para ambas operaciones, para restaurar y no para copias de seguridad, o para realizar copias de seguridad y no restaurar.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-119">Selectability for backup and selectability for restore are independent of each other—a component may be selectable for both operations, for restore and not backup, or for backup and not restore.</span></span>

<span data-ttu-id="e7eb2-120">Los escritores también usan la selección para organizar sus componentes en grupos:</span><span class="sxs-lookup"><span data-stu-id="e7eb2-120">Writers also use selectability to organize their components into groups:</span></span>

-   <span data-ttu-id="e7eb2-121">Siempre se deben incluir explícitamente los componentes no seleccionables sin antecesores seleccionables en sus rutas de acceso lógicas si se va a realizar la copia de seguridad o la restauración de un escritor.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-121">Nonselectable components with no selectable ancestors in their logical paths must always be explicitly included if a writer is to be backed up or restored.</span></span>
-   <span data-ttu-id="e7eb2-122">Los componentes no seleccionables con antecesores seleccionables solo se incluirán en una copia de seguridad o restauración si se incluye al menos un antecesor seleccionable.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-122">Nonselectable components with selectable ancestors will only be included in a backup or restore if at least one selectable ancestor is included.</span></span>
-   <span data-ttu-id="e7eb2-123">Los componentes seleccionables sin antecesores seleccionables solo se pueden incluir en una operación de copia de seguridad o restauración explícitamente.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-123">Selectable components without selectable ancestors can only be included in a backup or restore operation explicitly.</span></span>
-   <span data-ttu-id="e7eb2-124">Los componentes seleccionables con antecesores seleccionables se pueden incluir explícitamente en una operación de copia de seguridad o restauración, o se pueden incluir implícitamente si se incluye uno de sus antecesores seleccionables.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-124">Selectable components with selectable ancestors can be explicitly included in a backup or restore operation, or can be implicitly included if one of their selectable ancestors is included.</span></span>

<span data-ttu-id="e7eb2-125">Vea también [*componentes*](vssgloss-c.md), *selección de copia de seguridad*, *la selección de la restauración*, [*inclusión explícita de componentes*](vssgloss-e.md), [*inclusión implícita de componentes*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="e7eb2-125">See also [*components*](vssgloss-c.md), *selectability for backup*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**instantánea**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-127">Réplica en un momento dado de solo lectura del contenido de un volumen original.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-127">A read-only point-in-time replica of an original volume's contents.</span></span> <span data-ttu-id="e7eb2-128">Cada instantánea está ordenada por un GUID persistente.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-128">Each shadow copy is keyed by a persistent GUID.</span></span> <span data-ttu-id="e7eb2-129">También se denomina instantánea de volumen.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-129">Also called a volume shadow copy.</span></span> <span data-ttu-id="e7eb2-130">Vea también *conjunto de instantáneas*.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-130">See also *shadow copy set*.</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Instantáneas para carpetas compartidas**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Shadow Copies for Shared Folders**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-132">Característica de Windows que crea copias de seguridad ligeras en línea de volúmenes con VSS.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-132">A feature of Windows that creates lightweight, online backup copies of volumes using VSS.</span></span> <span data-ttu-id="e7eb2-133">Los clientes pueden tener acceso a estas copias de seguridad a través del shell de Windows para ver las versiones anteriores de los archivos y deshacer los errores sin necesidad de una restauración completa.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-133">Clients can access these backups through the Windows shell to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="e7eb2-134">Vea también [*instantánea accesible del cliente*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="e7eb2-134">See also [*client accessible shadow copy*](vssgloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**conjunto de instantáneas**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**shadow copy set**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-136">Colección de instantáneas de volumen creadas al mismo tiempo e identificadas por un valor común de identificador de conjunto de instantáneas (GUID persistente).</span><span class="sxs-lookup"><span data-stu-id="e7eb2-136">A collection of volume shadow copies created at the same time and identified by a common shadow copy set ID (a persistent GUID) value.</span></span> <span data-ttu-id="e7eb2-137">Este es el mecanismo que se usa para permitir la administración de una operación de instantáneas en los volúmenes.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-137">This is the mechanism used to allow a shadow copy operation to be managed across volumes.</span></span> <span data-ttu-id="e7eb2-138">Consulte también *instantánea*.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-138">See also *shadow copy*.</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**proveedor de software**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-140">Proveedor que intercepta las solicitudes de e/s en el nivel de software entre el sistema de archivos y el administrador de volúmenes.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-140">A provider that intercepts I/O requests at the software level between the file system and the volume manager.</span></span> <span data-ttu-id="e7eb2-141">Vea también [*proveedor de hardware*](vssgloss-h.md), [*proveedor*](vssgloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="e7eb2-141">See also [*hardware provider*](vssgloss-h.md), [*provider*](vssgloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**subcomponente**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**subcomponent**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-143">Cualquier componente que tenga una ruta de acceso lógica que contenga un componente primario seleccionable (para copia de seguridad o restauración).</span><span class="sxs-lookup"><span data-stu-id="e7eb2-143">Any component that has a logical path containing a selectable (for either backup or restore) parent component.</span></span> <span data-ttu-id="e7eb2-144">Los subcomponentes deben tener una ruta de acceso lógica con la forma {nombre de componente \_ } \\ {nombre de subcomponente \_ }.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-144">Subcomponents must have a logical path of the form {component\_name}\\{subcomponent\_name}.</span></span> <span data-ttu-id="e7eb2-145">Si el antecesor seleccionable de un subcomponente (para copia de seguridad o restauración) se incluye explícitamente en una copia de seguridad o restauración, el subcomponente se incluye implícitamente en la operación.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-145">If a subcomponent's selectable (for either backup or restore) ancestor is explicitly included in a backup or restore, then the subcomponent is implicitly included in the operation.</span></span> <span data-ttu-id="e7eb2-146">Los subcomponentes incluidos implícitamente no tienen sus datos incluidos en el documento componentes de copia de seguridad, independientemente de si son seleccionables (para restauración o copia de seguridad) o no.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-146">Implicitly included subcomponents do not have their data included in the Backup Components Document—regardless of whether they are selectable (for either restore or backup) or not.</span></span> <span data-ttu-id="e7eb2-147">Vea también [*componente*](vssgloss-c.md), [*ruta de acceso lógica*](vssgloss-l.md).</span><span class="sxs-lookup"><span data-stu-id="e7eb2-147">See also [*component*](vssgloss-c.md), [*logical path*](vssgloss-l.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**instantáneas superficiales**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**surfaced shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-149">Un volumen de copia sombra visible para el espacio de nombres del administrador de montaje de un sistema, lo que significa que **FindFirstVolume** y **FindNextVolume** pueden encontrarlo y que se generan notificaciones de llegada y salida de volumen.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-149">A shadow copied volume visible to a system's Mount Manager namespace—meaning **FindFirstVolume** and **FindNextVolume** can find it and that volume arrival and departure notifications are generated.</span></span> <span data-ttu-id="e7eb2-150">Todas las instantáneas expuestas también son instantáneas superficiales.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-150">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="e7eb2-151">Sin embargo, no es necesario exponer una instantánea superficial.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-151">However, a surfaced shadow copy need not be exposed.</span></span> <span data-ttu-id="e7eb2-152">Si una instantánea es transportable, no se puede mostrar.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-152">If a shadow copy is transportable, it cannot be surfaced.</span></span> <span data-ttu-id="e7eb2-153">Vea también instantáneas [*expuestas*](vssgloss-e.md), instantáneas [*transportables*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="e7eb2-153">See also [*exposed shadow copy*](vssgloss-e.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Protección de archivos del sistema**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**System File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-155">Consulte [*protección de archivos de Windows*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="e7eb2-155">See [*Windows File Protection*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**aplicaciones de nivel de sistema**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**system-level applications**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-157">Indica el punto en el que VSS notifica a un escritor de una inmovilización.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-157">Indicates the point at which VSS notifies a writer of a freeze.</span></span> <span data-ttu-id="e7eb2-158">Los escritores que se inicializan como aplicaciones de nivel de sistema se notifican después de que los escritores se inicialicen como aplicaciones de nivel de front-end o como aplicaciones de nivel de back-end.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-158">Writers that are initialized as system-level applications are notified after writers initialized either as front-end level applications or as back-end level applications.</span></span> <span data-ttu-id="e7eb2-159">Vea también [*nivel de aplicación*](vssgloss-a.md), [*aplicaciones de nivel de back-end*](vssgloss-b.md), [*aplicaciones de nivel de front-end*](vssgloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="e7eb2-159">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*front-end level applications*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**proveedor del sistema**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**system provider**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-161">El proveedor preinstalado predeterminado proporcionado como parte de Windows.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-161">The default preinstalled provider provided as part of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e7eb2-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Carpeta de volumen del sistema**</span><span class="sxs-lookup"><span data-stu-id="e7eb2-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**System Volume Folder**</span></span>
</dt> <dd>

<span data-ttu-id="e7eb2-163">Directorio compartido que almacena las copias compartidas de los archivos públicos de un dominio, es decir, los archivos que se replican entre todos los controladores de dominio del dominio.</span><span class="sxs-lookup"><span data-stu-id="e7eb2-163">A shared directory that stores the shared copies of a domain's public files—that is, those files that are replicated among all domain controllers in the domain.</span></span>

</dd> </dl>

 

 



