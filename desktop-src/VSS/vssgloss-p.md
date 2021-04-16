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
# <a name="p-volume-shadow-copy-service"></a><span data-ttu-id="36cb7-103">P (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="36cb7-103">P (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="36cb7-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) p Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="36cb7-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="36cb7-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**compatibilidad con archivos parciales**</span><span class="sxs-lookup"><span data-stu-id="36cb7-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**partial file support**</span></span>
</dt> <dd>

<span data-ttu-id="36cb7-106">La capacidad de implementar las operaciones de copia de seguridad mediante la modificación de subsecciones de los archivos implicados, en lugar de trabajar con los archivos completos.</span><span class="sxs-lookup"><span data-stu-id="36cb7-106">The capacity to implement backup operations by modifying subsections of the files involved, rather than working with the entire files.</span></span> <span data-ttu-id="36cb7-107">Vea también [*destinos dirigidos*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="36cb7-107">See also [*directed targeting*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="36cb7-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**instantánea persistente**</span><span class="sxs-lookup"><span data-stu-id="36cb7-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**persistent shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="36cb7-109">Una instantánea que no se elimina automáticamente cuando el solicitante libera un objeto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) o cuando se reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="36cb7-109">A shadow copy that is not deleted automatically when the requester releases an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object or when the computer is restarted.</span></span> <span data-ttu-id="36cb7-110">Vea también instantánea [*de versión automática*](vssgloss-a.md), instantánea [*.*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="36cb7-110">See also [*auto-release shadow copy*](vssgloss-a.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="36cb7-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Complejos**</span><span class="sxs-lookup"><span data-stu-id="36cb7-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plex**</span></span>
</dt> <dd>

<span data-ttu-id="36cb7-112">Un tipo especial de volumen de instantánea que representa completamente y completamente un volumen de instantáneas sin necesidad de un volumen original.</span><span class="sxs-lookup"><span data-stu-id="36cb7-112">A special type of shadow copy volume that fully and completely represents a shadow copy volume without the need for either original volume.</span></span> <span data-ttu-id="36cb7-113">Esto también se conoce normalmente como un reflejo dividido, pero en esta documentación se usa el término Plex.</span><span class="sxs-lookup"><span data-stu-id="36cb7-113">This is also commonly known as a split-mirror, but this documentation uses the term Plex.</span></span>

</dd> <dt>

<span data-ttu-id="36cb7-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**Postrestore, evento**</span><span class="sxs-lookup"><span data-stu-id="36cb7-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**PostRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="36cb7-115">Un evento de VSS que indica que se ha completado una restauración de VSS.</span><span class="sxs-lookup"><span data-stu-id="36cb7-115">A VSS event indicating that a VSS restore has completed.</span></span>

</dd> <dt>

<span data-ttu-id="36cb7-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**Evento postsnapshot**</span><span class="sxs-lookup"><span data-stu-id="36cb7-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**PostSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="36cb7-117">Un evento de VSS que indica que se ha completado una instantánea.</span><span class="sxs-lookup"><span data-stu-id="36cb7-117">A VSS event indicating that a shadow copy has been completed.</span></span> <span data-ttu-id="36cb7-118">Consulte también [*instantánea*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="36cb7-118">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="36cb7-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**Evento PrepareForBackup**</span><span class="sxs-lookup"><span data-stu-id="36cb7-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**PrepareForBackup event**</span></span>
</dt> <dd>

<span data-ttu-id="36cb7-120">Un evento de VSS que indica que está a punto de realizarse una operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="36cb7-120">A VSS event indicating that a backup operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="36cb7-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**Evento PrepareForSnapshot**</span><span class="sxs-lookup"><span data-stu-id="36cb7-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**PrepareForSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="36cb7-122">Un evento de VSS que indica que los escritores deben realizar pasos para preparar una próxima operación de instantánea.</span><span class="sxs-lookup"><span data-stu-id="36cb7-122">A VSS event indicating that writers should take steps to prepare for an upcoming shadow copy operation.</span></span> <span data-ttu-id="36cb7-123">Consulte también [*instantánea*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="36cb7-123">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="36cb7-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**Evento de prerestauración**</span><span class="sxs-lookup"><span data-stu-id="36cb7-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**PreRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="36cb7-125">Un evento de VSS que indica que está a punto de realizarse una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="36cb7-125">A VSS event indicating that a restore operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="36cb7-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**presta**</span><span class="sxs-lookup"><span data-stu-id="36cb7-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="36cb7-127">Objeto del sistema operativo que intercepta y administra las solicitudes de e/s para crear y representar instantáneas de volumen en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="36cb7-127">An operating system object that intercepts and manages I/O requests to create and represent volume shadow copies to the file system.</span></span> <span data-ttu-id="36cb7-128">Vea también [*proveedor de hardware*](vssgloss-h.md), [*proveedor de software*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="36cb7-128">See also [*hardware provider*](vssgloss-h.md), [*software provider*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



