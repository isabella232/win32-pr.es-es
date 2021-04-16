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
# <a name="e-volume-shadow-copy-service"></a>E (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**inclusión de componentes explícitos**
</dt> <dd>

Agregar información de un componente al documento de componentes de copia de seguridad del solicitante cuando participa en una operación de copia de seguridad o restauración. Los solicitantes usan [**ivssbackupcomponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para incluir explícitamente un componente en una operación de copia de seguridad y [**Ivssbackupcomponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) o [**ivssbackupcomponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) para incluir explícitamente un componente en una operación de restauración.

Si se realiza una copia de seguridad o se restaura algún componente de un escritor, todos los componentes no seleccionables sin antecesores seleccionables deben incluirse explícitamente en una operación de copia de seguridad o restauración.

Los componentes seleccionables sin antecesores seleccionables elegidos por un solicitante para participar en una copia de seguridad o restauración deben incluirse explícitamente en la operación.

Los componentes no seleccionables con un antecesor seleccionable nunca se incluyen explícitamente.

Los componentes seleccionables con un antecesor seleccionable se pueden incluir explícitamente o se pueden incluir implícitamente si el antecesor se incluye explícitamente.

</dd> <dt>

<span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**instantáneas expuestas**
</dt> <dd>

Instantánea de volumen que se monta en un sistema y que está disponible para los procesos distintos del que la administra. Un volumen de instantánea montado en una letra de unidad o en una ubicación de directorio se conoce como "expuesto localmente". Un volumen de instantáneas accesible a través de un recurso compartido (excepto para las instantáneas accesibles para el cliente) se conoce como "expuesto de forma remota". Todas las instantáneas expuestas también son instantáneas superficiales. Vea también [*instantánea accesible del cliente*](vssgloss-c.md), [*instantánea*](vssgloss-s.md).

</dd> </dl>

 

 



