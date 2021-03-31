---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f60a456ce6ea795dc8376c0f707d028523cec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809806"
---
# <a name="f-volume-shadow-copy-service"></a>F (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**componente de grupo de archivos**
</dt> <dd>

Grupo de archivos que no son los que se usan como base de datos y que define un escritor, ya que es necesario controlarlos como una unidad durante las operaciones de copia de seguridad y restauración. Vea también [*componente*](vssgloss-c.md), [*componente de base de datos*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**conjunto de archivos**
</dt> <dd>

Combinación de una ruta de acceso, especificación de archivo y marca recursiva que describe uno de un archivo o un grupo de archivos. Por ejemplo, los archivos se agregan a los componentes de los conjuntos de archivos.

A menos que se indique lo contrario, las rutas de acceso de un conjunto de archivos son rutas de Windows estándar y pueden contener variables de entorno (por ejemplo,% SystemRoot%) pero no puede contener caracteres comodín. No es necesario que la ruta de acceso finalice con una barra diagonal inversa (" \\ "). Depende de las aplicaciones que recuperan esta información para comprobarlo.

La especificación de archivo incluida en un conjunto de archivos indica el nombre del archivo o los archivos que incluye. Esta especificación de archivo no puede contener especificaciones de directorio (por ejemplo, sin barras diagonales inversas), pero puede contener el carácter? y \* caracteres comodín.

La etiqueta recursiva es un valor booleano que especifica si la ruta de acceso del conjunto de archivos se debe tratar como un solo directorio o si indica una jerarquía de directorios que se va a atravesar de forma recursiva. El valor booleano es **true** si la ruta de acceso se trata como una jerarquía de directorios que se va a recorrer de forma recursiva, o bien **false** en caso contrario.

La información sobre un conjunto de archivos se devuelve a través de instancias de la interfaz **IVssWMFiledesc** y puede contener información adicional que incluye rutas de acceso alternativas, asignaciones de ubicaciones alternativas y configuraciones de compatibilidad con esquemas de nivel de archivo.

Vea también [*ruta alternativa*](vssgloss-a.md), [*asignación de ubicación alternativa*](vssgloss-a.md), [*componente*](vssgloss-c.md), *especificación de archivo*.

</dd> <dt>

<span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**Especificación de archivo**
</dt> <dd>

Se usa para hacer coincidir los archivos de un directorio y definir un conjunto de archivos. No puede contener especificaciones de directorio (por ejemplo, sin barras diagonales inversas), pero puede contener el carácter? y \* caracteres comodín.

</dd> <dt>

<span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Servicio de replicación de archivos**
</dt> <dd>

Se usa para replicar archivos del sistema en un directorio de volumen del sistema (SysVol) redundante para admitir la supervivencia del sistema de archivos, especialmente en el caso de los sistemas de archivos distribuidos.

</dd> <dt>

<span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**Inmovilice**
</dt> <dd>

Un período de tiempo durante el proceso de creación de instantáneas cuando todos los escritores han vaciado sus escrituras en los volúmenes y no inician escrituras adicionales.

</dd> <dt>

<span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Evento Freeze**
</dt> <dd>

Un evento de VSS que indica que hay una inmovilización de instantáneas en curso. Vea también *inmovilizar*, [*instantánea*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**aplicaciones de nivel de front-end**
</dt> <dd>

Indica el punto en el que se notifica a un escritor de una inmovilización de VSS. Los escritores que se inicializaron como aplicaciones de nivel de front-end reciben una notificación antes de que los escritores se inicialicen como aplicaciones de nivel de back-end o como aplicaciones de nivel de sistema. Vea también [*nivel de aplicación*](vssgloss-a.md), [*aplicaciones de nivel de back-end*](vssgloss-b.md), [*aplicaciones de nivel de sistema*](vssgloss-s.md), [*escritor*](vssgloss-w.md).

</dd> </dl>

 

 



