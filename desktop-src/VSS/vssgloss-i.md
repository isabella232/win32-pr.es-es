---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b043c340de5d1703587b83f72851db76d367832a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809805"
---
# <a name="i-volume-shadow-copy-service"></a><span data-ttu-id="92275-103">I (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="92275-103">I (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="92275-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="92275-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="92275-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Evento de identificación**</span><span class="sxs-lookup"><span data-stu-id="92275-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identify event**</span></span>
</dt> <dd>

<span data-ttu-id="92275-106">Un evento de VSS que indica que un escritor o un solicitante necesita consultar el escritor actual.</span><span class="sxs-lookup"><span data-stu-id="92275-106">A VSS event indicating that a writer or a requester needs to query the current writer.</span></span> <span data-ttu-id="92275-107">Se utiliza para construir la información de metadatos del escritor actual.</span><span class="sxs-lookup"><span data-stu-id="92275-107">It is used to construct the current writer's metadata information.</span></span> <span data-ttu-id="92275-108">Vea también [*solicitante*](vssgloss-r.md), [*escritor*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="92275-108">See also [*requester*](vssgloss-r.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="92275-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**inclusión implícita de componentes**</span><span class="sxs-lookup"><span data-stu-id="92275-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**implicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="92275-110">No se agrega la información de un componente al documento de componentes de copia de seguridad del solicitante cuando participa en una operación de copia de seguridad o restauración.</span><span class="sxs-lookup"><span data-stu-id="92275-110">Not adding a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span>

<span data-ttu-id="92275-111">Los componentes no seleccionables con un antecesor seleccionable solo se incluyen implícitamente si se incluye su antecesor.</span><span class="sxs-lookup"><span data-stu-id="92275-111">Nonselectable components with a selectable ancestor are only implicitly included if their ancestor is included.</span></span>

<span data-ttu-id="92275-112">Los componentes seleccionables con un antecesor seleccionable se pueden incluir implícitamente, si el antecesor está incluido o se puede incluir explícitamente.</span><span class="sxs-lookup"><span data-stu-id="92275-112">Selectable components with a selectable ancestor may be included implicitly, if the ancestor is included, or may be included explicitly.</span></span>

<span data-ttu-id="92275-113">Los componentes no seleccionables sin antecesores seleccionables nunca se incluyen de forma implícita en una operación de copia de seguridad o restauración; todos estos componentes deben agregarse explícitamente al documento componentes de copia de seguridad si alguno de los componentes del escritor participa.</span><span class="sxs-lookup"><span data-stu-id="92275-113">Nonselectable components without any selectable ancestors are never implicitly included in a backup or restore operation—all such components must be explicitly added to the Backup Components Document if any of the writer's components participate.</span></span>

<span data-ttu-id="92275-114">Los componentes seleccionables sin antecesores seleccionables elegidos por un solicitante para participar en una copia de seguridad o restauración no se pueden incluir implícitamente en la operación, pero se deben agregar explícitamente al documento componentes de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="92275-114">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore cannot be implicitly included in the operation, but must be explicitly added to the Backup Components Document.</span></span>

</dd> <dt>

<span data-ttu-id="92275-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**operaciones de copia de seguridad incremental**</span><span class="sxs-lookup"><span data-stu-id="92275-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**incremental backup operations**</span></span>
</dt> <dd>

<span data-ttu-id="92275-116">Una operación de copia de seguridad o restauración se realiza solo en los archivos creados o modificados desde la última vez que se guardó la copia de seguridad completa, incremental o diferencial.</span><span class="sxs-lookup"><span data-stu-id="92275-116">A backup or restore operation is performed only on files created or changed since the last full, incremental, or differential backup was saved.</span></span> <span data-ttu-id="92275-117">Vea también [*operaciones de copia de seguridad diferenciales*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="92275-117">See also [*differential backup operations*](vssgloss-d.md).</span></span>

</dd> </dl>

 

 



