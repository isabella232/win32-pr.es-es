---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d858294c5647e62d1eb949b3fa336d3dcc513a9a374443e0fe9621f1721800
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986545"
---
# <a name="a-volume-shadow-copy-service"></a>A (Servicio de instantáneas de volumen)

A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Abort event**
</dt> <dd>

Evento vss emitido por el Servicio de instantáneas de volumen que indica que se ha anulado una operación de copia de seguridad o restauración compatible. El controlador de eventos **es CVssWriter::OnAbort**.

</dd> <dt>

<span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**
</dt> <dd>

Active Directory Service (ADSI) es un servicio basado en COM que proporciona un mecanismo para buscar, identificar y acceder a los usuarios y recursos disponibles en un sistema de entorno informático distribuido. En concreto, el servicio Active Directory se usa para administrar la información de directorios empresariales para su distribución por parte de un Windows dominio.

</dd> <dt>

<span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**asignación de ubicación alternativa**
</dt> <dd>

Una ruta de acceso, que no sea la ruta de acceso original de un archivo, en la que se puede restaurar el archivo en determinadas condiciones. Normalmente, las asignaciones de ubicación alternativas no se definen para un único archivo bien definido, sino para un par de especificación de ruta de acceso y archivo, y pueden ser recursivas.

Una asignación de ubicación alternativa solo se usa durante una operación de restauración y no debe confundirse con una ruta de acceso alternativa, que solo se usa durante una operación de copia de seguridad. Consulte también ruta *de acceso alternativa.*

</dd> <dt>

<span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**ruta de acceso alternativa**
</dt> <dd>

Durante las operaciones de copia de seguridad, se dice que un par de especificación de ruta de acceso y archivo (que controla una instancia de la interfaz **IVssWMFiledesc)** tiene una ruta de acceso alternativa si su descriptor de archivo (tal y como devuelve **IVssWMFiledesc::GetAlternateLocation)** no es NULL. Es a partir de esta ruta de acceso, en lugar de la ruta de acceso predeterminada especificada, que los archivos se copiarán cuando se haga una copia de seguridad de un volumen.

Una ruta de acceso alternativa solo se usa durante una operación de copia de seguridad y no debe confundirse con una asignación de ubicación alternativa. Solo se usa una asignación de ubicación alternativa durante las operaciones de restauración. Consulte también *asignación de ubicación alternativa.*

</dd> <dt>

<span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**nivel de aplicación**
</dt> <dd>

VsS lo usa para indicar el punto en el transcurso de la creación de una instantánea que notifica a un escritor una inmovilización. Vea también [*aplicaciones de nivel de back-end,*](vssgloss-b.md) [*inmovilizar,*](vssgloss-f.md)aplicaciones de nivel [*de front-end,*](vssgloss-f.md)instantáneas, [](vssgloss-s.md)aplicaciones de nivel de [*sistema*](vssgloss-s.md)y [*escritor.*](vssgloss-w.md)

</dd> <dt>

<span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**instantánea recuperada automáticamente**
</dt> <dd>

Una instantánea que ha tenido procesamiento adicional por parte de un escritor para que esté en un estado completamente coherente para las acciones de copia de seguridad o minería de datos (por ejemplo, revertir todas las transacciones que aún no se completaron en el momento en que se creó la instantánea). Esto lo puede iniciar un escritor especificando una marca adecuada de la enumeración **VSS \_ COMPONENT \_ FLAGS** en el miembro **dwComponentFlags** de la estructura **\_ COMPONENTINFO** de VSS o mediante un solicitante agregando la marca **\_ VSS VOLSNAP \_ ATTR \_ ROLLBACK \_ RECOVERY** al contexto de la instantánea. La recuperación automática permite que los datos copiados en la sombra se utilicen en un volumen de solo lectura, para minería de datos, restauraciones parciales (por ejemplo, elementos seleccionados en una base de datos) u otros fines.

Vea también [*instantánea transportable.*](vssgloss-t.md)

</dd> <dt>

<span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**instantánea de versión automática**
</dt> <dd>

Instantánea que se eliminará al finalizar una operación de copia de seguridad. Mediante programación, esto significa que la instantánea se eliminará cuando se libera la interfaz **IVssBackupComponents.** Una instantánea de versión automática no puede ser persistente.

De forma predeterminada, todas las instantáneas se liberan automáticamente. Vea también instantánea [*persistente*](vssgloss-p.md), [*instantánea transportable*](vssgloss-t.md).

</dd> </dl>

 

 



