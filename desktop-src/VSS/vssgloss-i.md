---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a672a8cd25792dedb6e32e0916e85ddf50634824b00491733e19bab2c30ece4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056182"
---
# <a name="i-volume-shadow-copy-service"></a>I (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) G [](vssgloss-g.md) [H I](vssgloss-h.md) J K [L M](vssgloss-l.md) N [](vssgloss-n.md) [O](vssgloss-o.md) [P P](vssgloss-p.md) [Q R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identificación del evento**
</dt> <dd>

Evento de VSS que indica que un escritor o solicitante necesita consultar el sistema de escritura actual. Se usa para construir la información de metadatos del escritor actual. Vea también [*solicitante ,*](vssgloss-r.md) [*escritor*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**inclusión implícita de componentes**
</dt> <dd>

No se agrega la información de un componente al documento componentes de copia de seguridad de un solicitante cuando participa en una operación de copia de seguridad o restauración.

Los componentes no seleccionables con un antecesor seleccionable solo se incluyen implícitamente si se incluye su antecesor.

Los componentes seleccionables con un antecesor seleccionable se pueden incluir implícitamente, si se incluye el antecesor o se pueden incluir explícitamente.

Los componentes no seleccionables sin antecesores seleccionables nunca se incluyen implícitamente en una operación de copia de seguridad o restauración: todos estos componentes deben agregarse explícitamente al documento Componentes de copia de seguridad si alguno de los componentes del escritor participa.

Los componentes seleccionables sin antecesores seleccionables elegidos por un solicitante para participar en una copia de seguridad o restauración no se pueden incluir implícitamente en la operación, pero deben agregarse explícitamente al documento Componentes de copia de seguridad.

</dd> <dt>

<span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**operaciones de copia de seguridad incrementales**
</dt> <dd>

Una operación de copia de seguridad o restauración solo se realiza en los archivos creados o modificados desde que se guardó la última copia de seguridad completa, incremental o diferencial. Consulte también Operaciones [*diferenciales de copia de seguridad*](vssgloss-d.md).

</dd> </dl>

 

 



