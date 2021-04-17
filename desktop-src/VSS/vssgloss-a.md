---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e654c0742c824ae7ad17d91e3a2ffa65c9e6bf77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696456"
---
# <a name="a-volume-shadow-copy-service"></a>A (Servicio de instantáneas de volumen)

A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Evento Abort**
</dt> <dd>

Un evento de VSS emitido por el Servicio de instantáneas de volumen que indica que se ha anulado una operación de copia de seguridad o restauración compatible. El controlador de eventos es **CVssWriter:: onabort**.

</dd> <dt>

<span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**
</dt> <dd>

Active Directory Service (ADSI) es un servicio basado en COM que proporciona un mecanismo para buscar, identificar y obtener acceso a los usuarios y recursos disponibles en un sistema de entorno informático distribuido. En concreto, el servicio Active Directory se utiliza para administrar la información de directorio de la empresa para su distribución por un servidor de dominio de Windows.

</dd> <dt>

<span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**asignación de ubicación alternativa**
</dt> <dd>

Una ruta de acceso, que no sea la ruta de acceso original de un archivo, a la que se puede restaurar el archivo en determinadas condiciones. Normalmente, las asignaciones de ubicación alternativas no se definen para un único archivo bien definido, sino para un par de especificación de ruta de acceso/archivo y pueden ser recursivas.

Una asignación de ubicación alternativa se usa solo durante una operación de restauración y no debe confundirse con una ruta de acceso alternativa, que solo se usa durante una operación de copia de seguridad. Vea también *ruta alternativa*.

</dd> <dt>

<span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**Ruta de acceso alternativa**
</dt> <dd>

Durante las operaciones de copia de seguridad, se dice que un par de especificación de ruta de acceso/archivo (controlado por una instancia de la interfaz **IVssWMFiledesc** ) tiene una ruta de acceso alternativa si su descriptor de archivo (devuelto por **IVssWMFiledesc:: GetAlternateLocation**) no es NULL. En esta ruta de acceso, en lugar de la ruta de acceso especificada predeterminada, los archivos se copiarán cuando se realice una copia de seguridad de un volumen.

Una ruta de acceso alternativa se usa solo durante una operación de copia de seguridad y no debe confundirse con una asignación de ubicación alternativa. Una asignación de ubicación alternativa se usa solo durante las operaciones de restauración. Vea también *asignación de ubicación alternativa*.

</dd> <dt>

<span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**nivel de aplicación**
</dt> <dd>

Lo usa VSS para indicar el punto en el transcurso de la creación de una instantánea a la que se notifica a un escritor de una inmovilización. Vea también [*aplicaciones de nivel de back-end*](vssgloss-b.md), [*inmovilizar*](vssgloss-f.md), [*aplicaciones de nivel de front-end*](vssgloss-f.md), [*instantáneas*](vssgloss-s.md), [*aplicaciones de nivel de sistema*](vssgloss-s.md), [*escritor*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**instantánea recuperada automáticamente**
</dt> <dd>

Una instantánea que ha tenido un procesamiento adicional por parte de un escritor para estar en un estado completamente coherente para las acciones de copia de seguridad o de minería de datos (por ejemplo, revertir todas las transacciones que aún no se han completado en el momento en que se creó la instantánea). Un escritor puede iniciar esto mediante la especificación de una marca adecuada de la enumeración de **\_ \_ marcas de componentes de VSS** en el miembro **dwComponentFlags** de la estructura **\_ COMPONENTINFO de VSS** o de un solicitante agregando la marca de **\_ \_ \_ \_ recuperación de reversión de atributo VOLSNAP de VSS** al contexto de la instantánea. La recuperación automática permite usar los datos de instantáneas en un volumen de solo lectura, en la minería de datos, en restauraciones parciales (por ejemplo, en los elementos seleccionados en una base de datos) o en otros propósitos.

Vea también [*instantáneas transportables*](vssgloss-t.md).

</dd> <dt>

<span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**instantánea de versión automática**
</dt> <dd>

Una instantánea que se eliminará tras la finalización de una operación de copia de seguridad. Mediante programación, esto significa que la instantánea se eliminará cuando se libere la interfaz **IVssBackupComponents** . Una instantánea de versión automática no puede ser persistente.

De forma predeterminada, todas las instantáneas se liberan automáticamente. Vea también [*instantáneas persistentes*](vssgloss-p.md), [*instantáneas transportables*](vssgloss-t.md).

</dd> </dl>

 

 



