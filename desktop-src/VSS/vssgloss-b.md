---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: B (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20cabdfa5260f65d1176f6f1d12ac1d805b9dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360313"
---
# <a name="b-volume-shadow-copy-service"></a><span data-ttu-id="05213-103">B (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="05213-103">B (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="05213-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="05213-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="05213-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**aplicaciones de nivel de back-end**</span><span class="sxs-lookup"><span data-stu-id="05213-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**back-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="05213-106">Indica el punto en el que se notifica a un escritor de una inmovilización de VSS.</span><span class="sxs-lookup"><span data-stu-id="05213-106">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="05213-107">Los escritores que se inicializan como aplicaciones de nivel de back-end reciben una notificación después de que los escritores se inicialicen como aplicaciones de nivel de front-end y antes de que se inicialicen como aplicaciones de nivel de sistema.</span><span class="sxs-lookup"><span data-stu-id="05213-107">Writers that are initialized as back-end level applications are notified after writers initialized as front-end level applications and prior to those initialized as system-level applications.</span></span> <span data-ttu-id="05213-108">Vea también [*nivel de aplicación*](vssgloss-a.md), [*aplicaciones de nivel de front-end*](vssgloss-f.md), [*aplicaciones de nivel de sistema*](vssgloss-s.md), [*escritor*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="05213-108">See also [*application level*](vssgloss-a.md), [*front-end level applications*](vssgloss-f.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="05213-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**Evento BackupComplete**</span><span class="sxs-lookup"><span data-stu-id="05213-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete event**</span></span>
</dt> <dd>

<span data-ttu-id="05213-110">Un evento de VSS que indica que se ha completado una copia de seguridad de VSS.</span><span class="sxs-lookup"><span data-stu-id="05213-110">A VSS event indicating that a VSS backup has completed.</span></span> <span data-ttu-id="05213-111">Este evento debe ir seguido de un evento BackupShutdown en un funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="05213-111">This event should be followed by a BackupShutdown event under normal operation.</span></span> <span data-ttu-id="05213-112">Vea también el *evento BackupShutdown*.</span><span class="sxs-lookup"><span data-stu-id="05213-112">See also *BackupShutdown event*.</span></span>

</dd> <dt>

<span data-ttu-id="05213-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Documento de componentes de copia de seguridad**</span><span class="sxs-lookup"><span data-stu-id="05213-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Backup Components Document**</span></span>
</dt> <dd>

<span data-ttu-id="05213-114">Documento XML creado por un solicitante (mediante la interfaz **IVssBackupComponents** ) en el transcurso de la configuración de una operación de restauración o de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="05213-114">An XML document created by a requester (using the **IVssBackupComponents** interface) in the course of setting up a restore or backup operation.</span></span> <span data-ttu-id="05213-115">El documento Componentes de copias de seguridad contiene una lista de los componentes incluidos explícitamente, de uno o varios escritores, que participan en una operación de copia de seguridad o restauración.</span><span class="sxs-lookup"><span data-stu-id="05213-115">The Backup Components Document contains a list of those explicitly included components, from one or more writers, participating in a backup or restore operation.</span></span> <span data-ttu-id="05213-116">No contiene información de los componentes incluidos implícitamente.</span><span class="sxs-lookup"><span data-stu-id="05213-116">It does not contain implicitly included component information.</span></span> <span data-ttu-id="05213-117">En cambio, un documento de metadatos de escritor solo contiene componentes de escritura que pueden participar en una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="05213-117">In contrast, a Writer Metadata Document contains only writer components that may participate in a backup.</span></span>

<span data-ttu-id="05213-118">Un documento de componentes de copia de seguridad se puede guardar en el disco.</span><span class="sxs-lookup"><span data-stu-id="05213-118">A Backup Components Document can be saved to disk.</span></span> <span data-ttu-id="05213-119">Vea también [*inclusión explícita de componentes*](vssgloss-e.md), [*inclusión implícita de componentes*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="05213-119">See also [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="05213-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**conjunto de copia de seguridad**</span><span class="sxs-lookup"><span data-stu-id="05213-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**backup set**</span></span>
</dt> <dd>

<span data-ttu-id="05213-121">Los archivos de los que se va a hacer una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="05213-121">Those files to be backed up.</span></span> <span data-ttu-id="05213-122">Incluye los archivos seleccionados por la inclusión en un componente, los indicados por las instrucciones include de nivel de escritor, menos los archivos que se han incluido explícitamente.</span><span class="sxs-lookup"><span data-stu-id="05213-122">It includes files selected by inclusion in a component, those indicated by writer-level include statements, less those files that have been explicitly included.</span></span>

</dd> <dt>

<span data-ttu-id="05213-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**Evento BackupShutdown**</span><span class="sxs-lookup"><span data-stu-id="05213-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown event**</span></span>
</dt> <dd>

<span data-ttu-id="05213-124">Un evento de VSS que indica que se ha cerrado una aplicación de copia de seguridad compatible.</span><span class="sxs-lookup"><span data-stu-id="05213-124">A VSS event indicating that a compliant backup application has shut down.</span></span> <span data-ttu-id="05213-125">Normalmente, está precedido por un evento BackupComplete.</span><span class="sxs-lookup"><span data-stu-id="05213-125">Normally, this is preceded by a BackupComplete event.</span></span> <span data-ttu-id="05213-126">Sin embargo, si una copia de seguridad finaliza de forma inesperada, este evento se puede generar sin un evento BackupComplete anterior.</span><span class="sxs-lookup"><span data-stu-id="05213-126">However, if a backup terminates unexpectedly, this event can be generated without a preceding BackupComplete event.</span></span> <span data-ttu-id="05213-127">Vea también el *evento BackupComplete*.</span><span class="sxs-lookup"><span data-stu-id="05213-127">See also *BackupComplete event*.</span></span>

</dd> <dt>

<span data-ttu-id="05213-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**marca de copia de seguridad**</span><span class="sxs-lookup"><span data-stu-id="05213-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**backup stamp**</span></span>
</dt> <dd>

<span data-ttu-id="05213-129">Cadena que contiene información sobre el momento en que se realizó una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="05213-129">A string containing information as to when a backup took place.</span></span> <span data-ttu-id="05213-130">VSS no impone ninguna restricción en el formato de esta cadena, salvo que es inteligible para todas las instancias del escritor de una clase determinada.</span><span class="sxs-lookup"><span data-stu-id="05213-130">VSS places no restriction on the format of this string, except that it be intelligible to all the writer instances of a given class.</span></span> <span data-ttu-id="05213-131">Puede contener información de fecha y hora, números de secuencia lógicos o cualquier otra información que permita que un escritor de la misma clase determine Cuándo tiene lugar la última copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="05213-131">It may contain time and date information, logical sequence numbers, or any other information that will allow a writer of the same class to determine when the last backup has take place.</span></span>

</dd> </dl>

 

 



