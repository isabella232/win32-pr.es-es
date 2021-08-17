---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2442a788-2e70-44c1-9c38-901c1c18a742
title: R (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31221211ee10672cd16298feb38f0005375afa5162ecc8fe5a2a92af32201bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751370"
---
# <a name="r-volume-shadow-copy-service"></a>R (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) H [](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N O](vssgloss-n.md) [](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**Solicitante**
</dt> <dd>

Como mínimo, cualquier proceso que interactúe con VSS para crear y administrar instantáneas y conjuntos de instantáneas de uno o varios volúmenes.

Normalmente, un solicitante administra instantáneas para admitir otras funcionalidades, como las operaciones de copia de seguridad y restauración y la creación de reflejo del disco. Vea también [*shadow copy*](vssgloss-s.md), shadow [*copy set*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**método restore**
</dt> <dd>

Especificación del método de proceso de restauración. Controla problemas como si los archivos se sobrescriben durante la restauración. Si una configuración del método de restauración está en conflicto con las del destino de restauración, el destino de restauración tiene prioridad. Vea también restaurar *destino*.

</dd> <dt>

<span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**destino de restauración**
</dt> <dd>

En VSS, un destino de restauración es una especificación de cómo un solicitante debe restaurar un archivo, por ejemplo, si debe sobrescribir los archivos existentes.

</dd> </dl>

 

 



