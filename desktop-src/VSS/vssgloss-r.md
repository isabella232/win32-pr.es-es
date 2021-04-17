---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2442a788-2e70-44c1-9c38-901c1c18a742
title: R (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5846454ef5d58acf8f1c546b5e1bbce379d0b103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696449"
---
# <a name="r-volume-shadow-copy-service"></a><span data-ttu-id="a7bbb-103">R (Servicio de instantáneas de volumen)</span><span class="sxs-lookup"><span data-stu-id="a7bbb-103">R (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="a7bbb-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q R [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="a7bbb-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a7bbb-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**solicitante**</span><span class="sxs-lookup"><span data-stu-id="a7bbb-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**requester**</span></span>
</dt> <dd>

<span data-ttu-id="a7bbb-106">Como mínimo, cualquier proceso que interactúe con VSS para crear y administrar instantáneas y conjuntos de instantáneas de uno o más volúmenes.</span><span class="sxs-lookup"><span data-stu-id="a7bbb-106">Minimally, any process that interacts with VSS to create and manage shadow copies and shadow copy sets of one or more volumes.</span></span>

<span data-ttu-id="a7bbb-107">Normalmente, un solicitante administra las instantáneas para admitir otras funciones, como operaciones de copia de seguridad y restauración y creación de reflejo de disco.</span><span class="sxs-lookup"><span data-stu-id="a7bbb-107">Typically, a requester manages shadow copies to support some other functionality, such as backup and restore operations and disk mirroring.</span></span> <span data-ttu-id="a7bbb-108">Vea también [*instantánea*](vssgloss-s.md), [*conjunto de instantáneas*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="a7bbb-108">See also [*shadow copy*](vssgloss-s.md), [*shadow copy set*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7bbb-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**Restore (método)**</span><span class="sxs-lookup"><span data-stu-id="a7bbb-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**restore method**</span></span>
</dt> <dd>

<span data-ttu-id="a7bbb-110">Especificación del método de proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="a7bbb-110">A specification of the restore process method.</span></span> <span data-ttu-id="a7bbb-111">Controla estos problemas como si los archivos se sobrescriben en la restauración.</span><span class="sxs-lookup"><span data-stu-id="a7bbb-111">It controls such issues as whether files are overwritten on restore.</span></span> <span data-ttu-id="a7bbb-112">Si una configuración de método de restauración está en conflicto con la del destino de restauración, el destino de restauración tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="a7bbb-112">If a restore method setting is in conflict with those of the restore target, then the restore target takes precedence.</span></span> <span data-ttu-id="a7bbb-113">Vea también *destino de restauración*.</span><span class="sxs-lookup"><span data-stu-id="a7bbb-113">See also *restore target*.</span></span>

</dd> <dt>

<span data-ttu-id="a7bbb-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**destino de restauración**</span><span class="sxs-lookup"><span data-stu-id="a7bbb-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**restore target**</span></span>
</dt> <dd>

<span data-ttu-id="a7bbb-115">En VSS, un destino de restauración es una especificación de cómo un solicitante debe restaurar un archivo, por ejemplo, si debe sobrescribir los archivos existentes.</span><span class="sxs-lookup"><span data-stu-id="a7bbb-115">Under VSS, a restore target is a specification of how a requester should restore a file, for example, if it should overwrite existing files.</span></span>

</dd> </dl>

 

 



