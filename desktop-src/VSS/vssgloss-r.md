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
# <a name="r-volume-shadow-copy-service"></a>R (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q R [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**solicitante**
</dt> <dd>

Como mínimo, cualquier proceso que interactúe con VSS para crear y administrar instantáneas y conjuntos de instantáneas de uno o más volúmenes.

Normalmente, un solicitante administra las instantáneas para admitir otras funciones, como operaciones de copia de seguridad y restauración y creación de reflejo de disco. Vea también [*instantánea*](vssgloss-s.md), [*conjunto de instantáneas*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**Restore (método)**
</dt> <dd>

Especificación del método de proceso de restauración. Controla estos problemas como si los archivos se sobrescriben en la restauración. Si una configuración de método de restauración está en conflicto con la del destino de restauración, el destino de restauración tiene prioridad. Vea también *destino de restauración*.

</dd> <dt>

<span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**destino de restauración**
</dt> <dd>

En VSS, un destino de restauración es una especificación de cómo un solicitante debe restaurar un archivo, por ejemplo, si debe sobrescribir los archivos existentes.

</dd> </dl>

 

 



