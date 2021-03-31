---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809817"
---
# <a name="c-volume-shadow-copy-service"></a><span data-ttu-id="d82c3-103">C (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="d82c3-103">C (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="d82c3-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="d82c3-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d82c3-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**entidad de certificación**</span><span class="sxs-lookup"><span data-stu-id="d82c3-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="d82c3-106">Una entidad de confianza para emitir certificados que impongan que el destinatario individual, equipo u organización que solicita el certificado cumple las condiciones de una directiva establecida.</span><span class="sxs-lookup"><span data-stu-id="d82c3-106">An entity entrusted to issue certificates asserting that the recipient individual, machine, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="d82c3-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**instantánea accesible para el cliente**</span><span class="sxs-lookup"><span data-stu-id="d82c3-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**client-accessible shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="d82c3-108">Una instantánea creada por el proveedor del sistema para admitir Instantáneas para carpetas compartidas y otros mecanismos de reversión, que permiten a los clientes ver las versiones anteriores de los archivos y deshacer los errores sin necesidad de una restauración completa.</span><span class="sxs-lookup"><span data-stu-id="d82c3-108">A shadow copy created by the system provider to support Shadow Copies for Shared Folders and other rollback mechanisms, which allow clients to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="d82c3-109">Una instantánea accesible para el cliente se crea mediante el **valor \_ \_ \_ accesible del cliente de VSS CTX** de la enumeración de [**\_ \_ \_ contexto de instantáneas de VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) .</span><span class="sxs-lookup"><span data-stu-id="d82c3-109">A client-accessible shadow copy is created using the **VSS\_CTX\_CLIENT\_ACCESSIBLE** value of the [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) enumeration.</span></span> <span data-ttu-id="d82c3-110">Además, el \_ \_ \_ valor accesible del cliente de atributo VOLSNAP \_ de VSS de la enumeración de [**\_ \_ \_ \_ atributos de instantáneas de volumen de VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) se establece automáticamente para las instantáneas accesibles para el cliente.</span><span class="sxs-lookup"><span data-stu-id="d82c3-110">In addition, the VSS\_VOLSNAP\_ATTR\_CLIENT\_ACCESSIBLE value of the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration is set automatically for client-accessible shadow copies.</span></span> <span data-ttu-id="d82c3-111">Vea también [*instantáneas para carpetas compartidas*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="d82c3-111">See also [*Shadow Copies for Shared Folders*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="d82c3-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**pone**</span><span class="sxs-lookup"><span data-stu-id="d82c3-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="d82c3-113">Grupo de archivos, definido por un escritor, que se debe administrar como una unidad durante las operaciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="d82c3-113">A group of files, defined by a writer, that must be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="d82c3-114">Vea también [*componente de base de datos*](vssgloss-d.md), [*componente de grupo de archivos*](vssgloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="d82c3-114">See also [*database component*](vssgloss-d.md), [*file group component*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="d82c3-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**dependencia de componentes**</span><span class="sxs-lookup"><span data-stu-id="d82c3-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**component dependency**</span></span>
</dt> <dd>

<span data-ttu-id="d82c3-116">Una situación en la que no se puede hacer una copia de seguridad de un componente (y el conjunto de componentes que define) administrado por un escritor no se puede realizar ni restaurar independientemente de los componentes administrados por otros escritores.</span><span class="sxs-lookup"><span data-stu-id="d82c3-116">A situation in which a component (and the component set it defines) managed by one writer cannot be backed up or restore independently of components managed by others writers.</span></span> <span data-ttu-id="d82c3-117">Una dependencia no indica un orden de preferencia entre el componente con las dependencias documentadas y los componentes de los que depende: una dependencia simplemente indica que el componente y los componentes de los que depende deben ser siempre copiados o restaurados juntos.</span><span class="sxs-lookup"><span data-stu-id="d82c3-117">A dependency does not indicate an order of preference between the component with the documented dependencies and the components it depends on: a dependency merely indicates that the component and the components it depends on must always be backed up or restored together.</span></span>

</dd> <dt>

<span data-ttu-id="d82c3-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**modo de componente**</span><span class="sxs-lookup"><span data-stu-id="d82c3-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**component mode**</span></span>
</dt> <dd>

<span data-ttu-id="d82c3-119">Modo en el que una operación de copia de seguridad o restauración hace uso de la información del componente de un escritor.</span><span class="sxs-lookup"><span data-stu-id="d82c3-119">A mode in which a backup or restore operation makes use of a writer's component information.</span></span> <span data-ttu-id="d82c3-120">Vea también [*componente seleccionable*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="d82c3-120">See also [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="d82c3-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**conjunto de componentes**</span><span class="sxs-lookup"><span data-stu-id="d82c3-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**component set**</span></span>
</dt> <dd>

<span data-ttu-id="d82c3-122">Grupo de componentes con al menos un componente seleccionable (para copia de seguridad o restauración) y varios componentes no seleccionables organizados en una jerarquía por sus rutas de acceso lógicas.</span><span class="sxs-lookup"><span data-stu-id="d82c3-122">A group of components with at least one selectable (for either backup or restore) component and a number of nonselectable components organized in a hierarchy by their logical paths.</span></span> <span data-ttu-id="d82c3-123">La participación implícita en una operación de copia de seguridad o restauración depende de la inclusión explícita del componente seleccionable de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="d82c3-123">The implicit participation in a backup or restore operation depends on the explicit inclusion of the top-level selectable component.</span></span> <span data-ttu-id="d82c3-124">En el documento componentes de copia de seguridad solo se incluye la información de componentes de este componente seleccionable.</span><span class="sxs-lookup"><span data-stu-id="d82c3-124">Only the component information of this selectable component is included in the Backup Components Document.</span></span> <span data-ttu-id="d82c3-125">Un conjunto de componentes puede incluir subcomponentes seleccionables y no seleccionables.</span><span class="sxs-lookup"><span data-stu-id="d82c3-125">A component set may include selectable and nonselectable subcomponents.</span></span> <span data-ttu-id="d82c3-126">Vea también [*ruta de acceso lógica*](vssgloss-l.md), [*componente seleccionable*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="d82c3-126">See also [*logical path*](vssgloss-l.md), [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="d82c3-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copia instantánea en escritura**</span><span class="sxs-lookup"><span data-stu-id="d82c3-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copy-on-write shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="d82c3-128">Una instantánea que se crea al guardar solo las diferencias del volumen original.</span><span class="sxs-lookup"><span data-stu-id="d82c3-128">A shadow copy created by saving only the differences from the original volume.</span></span>

</dd> <dt>

<span data-ttu-id="d82c3-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**estado coherente con el bloqueo**</span><span class="sxs-lookup"><span data-stu-id="d82c3-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**crash consistent state**</span></span>
</dt> <dd>

<span data-ttu-id="d82c3-130">El estado de los discos equivalente a lo que se encontraría después de un error catastrófico que apaga repentinamente el sistema.</span><span class="sxs-lookup"><span data-stu-id="d82c3-130">The state of disks equivalent to what would be found following a catastrophic failure that abruptly shuts down the system.</span></span> <span data-ttu-id="d82c3-131">Una restauración de este conjunto de instantáneas sería equivalente a un reinicio después de un apagado brusco.</span><span class="sxs-lookup"><span data-stu-id="d82c3-131">A restore from such a shadow copy set would be equivalent to a reboot following an abrupt shutdown.</span></span> <span data-ttu-id="d82c3-132">Este es el estado predeterminado de los datos de los que se ha realizado una copia sombra sin la compatibilidad de escritores.</span><span class="sxs-lookup"><span data-stu-id="d82c3-132">This is the default state of data that has been shadow copied without the support of writers.</span></span>

</dd> </dl>

 

 



