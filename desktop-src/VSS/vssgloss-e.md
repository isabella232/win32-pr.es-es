---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97425100d8e2e3d0add6ea0e6fd1de67bc6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696453"
---
# <a name="e-volume-shadow-copy-service"></a><span data-ttu-id="26ff6-103">E (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="26ff6-103">E (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="26ff6-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="26ff6-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="26ff6-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**inclusión de componentes explícitos**</span><span class="sxs-lookup"><span data-stu-id="26ff6-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**explicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="26ff6-106">Agregar información de un componente al documento de componentes de copia de seguridad del solicitante cuando participa en una operación de copia de seguridad o restauración.</span><span class="sxs-lookup"><span data-stu-id="26ff6-106">Adding of a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span> <span data-ttu-id="26ff6-107">Los solicitantes usan [**ivssbackupcomponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para incluir explícitamente un componente en una operación de copia de seguridad y [**Ivssbackupcomponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) o [**ivssbackupcomponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) para incluir explícitamente un componente en una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="26ff6-107">Requesters use [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to explicitly include a component in a backup operation, and [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) or [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) to explicitly include a component in a restore operation.</span></span>

<span data-ttu-id="26ff6-108">Si se realiza una copia de seguridad o se restaura algún componente de un escritor, todos los componentes no seleccionables sin antecesores seleccionables deben incluirse explícitamente en una operación de copia de seguridad o restauración.</span><span class="sxs-lookup"><span data-stu-id="26ff6-108">If any component of a writer is backed up or restored, all nonselectable components without any selectable ancestors must be explicitly included in a backup or restore operation.</span></span>

<span data-ttu-id="26ff6-109">Los componentes seleccionables sin antecesores seleccionables elegidos por un solicitante para participar en una copia de seguridad o restauración deben incluirse explícitamente en la operación.</span><span class="sxs-lookup"><span data-stu-id="26ff6-109">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore must be explicitly included in the operation.</span></span>

<span data-ttu-id="26ff6-110">Los componentes no seleccionables con un antecesor seleccionable nunca se incluyen explícitamente.</span><span class="sxs-lookup"><span data-stu-id="26ff6-110">Nonselectable components with a selectable ancestor are never explicitly included.</span></span>

<span data-ttu-id="26ff6-111">Los componentes seleccionables con un antecesor seleccionable se pueden incluir explícitamente o se pueden incluir implícitamente si el antecesor se incluye explícitamente.</span><span class="sxs-lookup"><span data-stu-id="26ff6-111">Selectable components with a selectable ancestor may be included explicitly, or may be included implicitly if the ancestor is included explicitly.</span></span>

</dd> <dt>

<span data-ttu-id="26ff6-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**instantáneas expuestas**</span><span class="sxs-lookup"><span data-stu-id="26ff6-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**exposed shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="26ff6-113">Instantánea de volumen que se monta en un sistema y que está disponible para los procesos distintos del que la administra.</span><span class="sxs-lookup"><span data-stu-id="26ff6-113">A volume shadow copy that is mounted on a system and available to processes other than the one that manages it.</span></span> <span data-ttu-id="26ff6-114">Un volumen de instantánea montado en una letra de unidad o en una ubicación de directorio se conoce como "expuesto localmente".</span><span class="sxs-lookup"><span data-stu-id="26ff6-114">A shadow copy volume mounted under a drive letter or a directory location is referred to as "locally exposed."</span></span> <span data-ttu-id="26ff6-115">Un volumen de instantáneas accesible a través de un recurso compartido (excepto para las instantáneas accesibles para el cliente) se conoce como "expuesto de forma remota".</span><span class="sxs-lookup"><span data-stu-id="26ff6-115">A shadow copy volume accessible through a share (except for client-accessible shadow copies) is referred to as "remotely exposed."</span></span> <span data-ttu-id="26ff6-116">Todas las instantáneas expuestas también son instantáneas superficiales.</span><span class="sxs-lookup"><span data-stu-id="26ff6-116">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="26ff6-117">Vea también [*instantánea accesible del cliente*](vssgloss-c.md), [*instantánea*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="26ff6-117">See also [*client accessible shadow copy*](vssgloss-c.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



