---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 305a02633e8ed2aca1e372f250d6d91a8560ef1cb7a9f565e64aea6924397ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905135"
---
# <a name="e-volume-shadow-copy-service"></a>E (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) G [H](vssgloss-g.md) [](vssgloss-h.md) [I](vssgloss-i.md) J K [L M](vssgloss-l.md) N [O](vssgloss-n.md) [](vssgloss-o.md) [P P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**inclusión explícita de componentes**
</dt> <dd>

Agregar la información de un componente al documento componentes de copia de seguridad de un solicitante cuando participa en una operación de copia de seguridad o restauración. Los solicitantes usan [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para incluir explícitamente un componente en una operación de copia de seguridad e [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) o [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) para incluir explícitamente un componente en una operación de restauración.

Si se hace una copia de seguridad de algún componente de un sistema de escritura o se restaura, todos los componentes no seleccionables sin antecesores seleccionables deben incluirse explícitamente en una operación de copia de seguridad o restauración.

Los componentes seleccionables sin antecesores seleccionables elegidos por un solicitante para participar en una copia de seguridad o restauración deben incluirse explícitamente en la operación.

Los componentes no seleccionables con un antecesor seleccionable nunca se incluyen explícitamente.

Los componentes seleccionables con un antecesor seleccionable se pueden incluir explícitamente o se pueden incluir implícitamente si el antecesor se incluye explícitamente.

</dd> <dt>

<span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**instantánea expuesta**
</dt> <dd>

Instantánea de volumen que se monta en un sistema y está disponible para procesos distintos del que la administra. Un volumen de instantánea montado bajo una letra de unidad o una ubicación de directorio se conoce como "expuesto localmente". Un volumen de instantáneas accesible a través de un recurso compartido (excepto las instantáneas accesibles por el cliente) se conoce como "expuesto de forma remota". Todas las instantáneas expuestas también son instantáneas expuestas. Consulte también [*instantáneas accesibles para el*](vssgloss-c.md)cliente, [*instantáneas*](vssgloss-s.md).

</dd> </dl>

 

 



