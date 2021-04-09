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
# <a name="i-volume-shadow-copy-service"></a>I (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Evento de identificación**
</dt> <dd>

Un evento de VSS que indica que un escritor o un solicitante necesita consultar el escritor actual. Se utiliza para construir la información de metadatos del escritor actual. Vea también [*solicitante*](vssgloss-r.md), [*escritor*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**inclusión implícita de componentes**
</dt> <dd>

No se agrega la información de un componente al documento de componentes de copia de seguridad del solicitante cuando participa en una operación de copia de seguridad o restauración.

Los componentes no seleccionables con un antecesor seleccionable solo se incluyen implícitamente si se incluye su antecesor.

Los componentes seleccionables con un antecesor seleccionable se pueden incluir implícitamente, si el antecesor está incluido o se puede incluir explícitamente.

Los componentes no seleccionables sin antecesores seleccionables nunca se incluyen de forma implícita en una operación de copia de seguridad o restauración; todos estos componentes deben agregarse explícitamente al documento componentes de copia de seguridad si alguno de los componentes del escritor participa.

Los componentes seleccionables sin antecesores seleccionables elegidos por un solicitante para participar en una copia de seguridad o restauración no se pueden incluir implícitamente en la operación, pero se deben agregar explícitamente al documento componentes de copia de seguridad.

</dd> <dt>

<span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**operaciones de copia de seguridad incremental**
</dt> <dd>

Una operación de copia de seguridad o restauración se realiza solo en los archivos creados o modificados desde la última vez que se guardó la copia de seguridad completa, incremental o diferencial. Vea también [*operaciones de copia de seguridad diferenciales*](vssgloss-d.md).

</dd> </dl>

 

 



