---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e654c0742c824ae7ad17d91e3a2ffa65c9e6bf77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696456"
---
# <a name="a-volume-shadow-copy-service"></a><span data-ttu-id="7905b-103">A (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="7905b-103">A (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="7905b-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="7905b-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="7905b-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Evento Abort**</span><span class="sxs-lookup"><span data-stu-id="7905b-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Abort event**</span></span>
</dt> <dd>

<span data-ttu-id="7905b-106">Un evento de VSS emitido por el Servicio de instantáneas de volumen que indica que se ha anulado una operación de copia de seguridad o restauración compatible.</span><span class="sxs-lookup"><span data-stu-id="7905b-106">A VSS event issued by the Volume Shadow Copy Service indicating that a compliant backup or restore operation has been aborted.</span></span> <span data-ttu-id="7905b-107">El controlador de eventos es **CVssWriter:: onabort**.</span><span class="sxs-lookup"><span data-stu-id="7905b-107">The event handler is **CVssWriter::OnAbort**.</span></span>

</dd> <dt>

<span data-ttu-id="7905b-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="7905b-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span></span>
</dt> <dd>

<span data-ttu-id="7905b-109">Active Directory Service (ADSI) es un servicio basado en COM que proporciona un mecanismo para buscar, identificar y obtener acceso a los usuarios y recursos disponibles en un sistema de entorno informático distribuido.</span><span class="sxs-lookup"><span data-stu-id="7905b-109">Active Directory Service (ADSI) is a COM-based service providing a mechanism for locating, identifying, and accessing the users and resources available in a distributed computing environment system.</span></span> <span data-ttu-id="7905b-110">En concreto, el servicio Active Directory se utiliza para administrar la información de directorio de la empresa para su distribución por un servidor de dominio de Windows.</span><span class="sxs-lookup"><span data-stu-id="7905b-110">In particular, the Active Directory service is used to manage enterprise directory information for distribution by a Windows domain server.</span></span>

</dd> <dt>

<span data-ttu-id="7905b-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**asignación de ubicación alternativa**</span><span class="sxs-lookup"><span data-stu-id="7905b-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**alternate location mapping**</span></span>
</dt> <dd>

<span data-ttu-id="7905b-112">Una ruta de acceso, que no sea la ruta de acceso original de un archivo, a la que se puede restaurar el archivo en determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="7905b-112">A path, other than a file's original path, to which the file may be restored under certain conditions.</span></span> <span data-ttu-id="7905b-113">Normalmente, las asignaciones de ubicación alternativas no se definen para un único archivo bien definido, sino para un par de especificación de ruta de acceso/archivo y pueden ser recursivas.</span><span class="sxs-lookup"><span data-stu-id="7905b-113">Typically, alternate location mappings are not defined for a single well-defined file, but for a path/file specification pair, and may be recursive.</span></span>

<span data-ttu-id="7905b-114">Una asignación de ubicación alternativa se usa solo durante una operación de restauración y no debe confundirse con una ruta de acceso alternativa, que solo se usa durante una operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7905b-114">An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.</span></span> <span data-ttu-id="7905b-115">Vea también *ruta alternativa*.</span><span class="sxs-lookup"><span data-stu-id="7905b-115">See also *alternate path*.</span></span>

</dd> <dt>

<span data-ttu-id="7905b-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**Ruta de acceso alternativa**</span><span class="sxs-lookup"><span data-stu-id="7905b-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**alternate path**</span></span>
</dt> <dd>

<span data-ttu-id="7905b-117">Durante las operaciones de copia de seguridad, se dice que un par de especificación de ruta de acceso/archivo (controlado por una instancia de la interfaz **IVssWMFiledesc** ) tiene una ruta de acceso alternativa si su descriptor de archivo (devuelto por **IVssWMFiledesc:: GetAlternateLocation**) no es NULL.</span><span class="sxs-lookup"><span data-stu-id="7905b-117">During backup operations, a path/file specification pair (handled by an instance of the **IVssWMFiledesc** interface) is said to have an alternate path if its file descriptor (as returned by **IVssWMFiledesc::GetAlternateLocation**) is non-NULL.</span></span> <span data-ttu-id="7905b-118">En esta ruta de acceso, en lugar de la ruta de acceso especificada predeterminada, los archivos se copiarán cuando se realice una copia de seguridad de un volumen.</span><span class="sxs-lookup"><span data-stu-id="7905b-118">It is from this path, rather than the default specified path, that files are to be copied when a volume is backed up.</span></span>

<span data-ttu-id="7905b-119">Una ruta de acceso alternativa se usa solo durante una operación de copia de seguridad y no debe confundirse con una asignación de ubicación alternativa.</span><span class="sxs-lookup"><span data-stu-id="7905b-119">An alternate path is used only during a backup operation and should not be confused with an alternate location mapping.</span></span> <span data-ttu-id="7905b-120">Una asignación de ubicación alternativa se usa solo durante las operaciones de restauración.</span><span class="sxs-lookup"><span data-stu-id="7905b-120">An alternate location mapping is used only during restore operations.</span></span> <span data-ttu-id="7905b-121">Vea también *asignación de ubicación alternativa*.</span><span class="sxs-lookup"><span data-stu-id="7905b-121">See also *alternate location mapping*.</span></span>

</dd> <dt>

<span data-ttu-id="7905b-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**nivel de aplicación**</span><span class="sxs-lookup"><span data-stu-id="7905b-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**application level**</span></span>
</dt> <dd>

<span data-ttu-id="7905b-123">Lo usa VSS para indicar el punto en el transcurso de la creación de una instantánea a la que se notifica a un escritor de una inmovilización.</span><span class="sxs-lookup"><span data-stu-id="7905b-123">Used by VSS to indicate the point in the course of the creation of a shadow copy that a writer is notified of a freeze.</span></span> <span data-ttu-id="7905b-124">Vea también [*aplicaciones de nivel de back-end*](vssgloss-b.md), [*inmovilizar*](vssgloss-f.md), [*aplicaciones de nivel de front-end*](vssgloss-f.md), [*instantáneas*](vssgloss-s.md), [*aplicaciones de nivel de sistema*](vssgloss-s.md), [*escritor*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="7905b-124">See also [*back-end level applications*](vssgloss-b.md), [*freeze*](vssgloss-f.md), [*front-end level applications*](vssgloss-f.md), [*shadow copy*](vssgloss-s.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905b-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**instantánea recuperada automáticamente**</span><span class="sxs-lookup"><span data-stu-id="7905b-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**auto-recovered shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="7905b-126">Una instantánea que ha tenido un procesamiento adicional por parte de un escritor para estar en un estado completamente coherente para las acciones de copia de seguridad o de minería de datos (por ejemplo, revertir todas las transacciones que aún no se han completado en el momento en que se creó la instantánea). Un escritor puede iniciar esto mediante la especificación de una marca adecuada de la enumeración de **\_ \_ marcas de componentes de VSS** en el miembro **dwComponentFlags** de la estructura **\_ COMPONENTINFO de VSS** o de un solicitante agregando la marca de **\_ \_ \_ \_ recuperación de reversión de atributo VOLSNAP de VSS** al contexto de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="7905b-126">A shadow copy that has had additional processing by a writer to be in a completely consistent state for backup or data mining actions (for example, rolling back all transactions that did not yet complete at the point that the shadow copy was created.) This can be initiated by a writer by specifying an appropriate flag from the **VSS\_COMPONENT\_FLAGS** enumeration in the **dwComponentFlags** member of the **VSS\_COMPONENTINFO** structure or by a requester by adding the **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** flag to the context for the shadow copy.</span></span> <span data-ttu-id="7905b-127">La recuperación automática permite usar los datos de instantáneas en un volumen de solo lectura, en la minería de datos, en restauraciones parciales (por ejemplo, en los elementos seleccionados en una base de datos) o en otros propósitos.</span><span class="sxs-lookup"><span data-stu-id="7905b-127">Auto-recovery allows the shadow copied data to be used on a read-only volume, for data mining, partial restores (for example selected items in a database), or other purposes.</span></span>

<span data-ttu-id="7905b-128">Vea también [*instantáneas transportables*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="7905b-128">See also [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905b-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**instantánea de versión automática**</span><span class="sxs-lookup"><span data-stu-id="7905b-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**auto-release shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="7905b-130">Una instantánea que se eliminará tras la finalización de una operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="7905b-130">A shadow copy that will be deleted upon the termination of a backup operation.</span></span> <span data-ttu-id="7905b-131">Mediante programación, esto significa que la instantánea se eliminará cuando se libere la interfaz **IVssBackupComponents** .</span><span class="sxs-lookup"><span data-stu-id="7905b-131">Programmatically, this means the shadow copy will be deleted when the **IVssBackupComponents** interface is released.</span></span> <span data-ttu-id="7905b-132">Una instantánea de versión automática no puede ser persistente.</span><span class="sxs-lookup"><span data-stu-id="7905b-132">An auto-release shadow copy cannot be persistent.</span></span>

<span data-ttu-id="7905b-133">De forma predeterminada, todas las instantáneas se liberan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7905b-133">By default, all shadow copies are auto-release.</span></span> <span data-ttu-id="7905b-134">Vea también [*instantáneas persistentes*](vssgloss-p.md), [*instantáneas transportables*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="7905b-134">See also [*persistent shadow copy*](vssgloss-p.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> </dl>

 

 



