---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56eef69a16a77fce7f557ae0ff02ff0e5d84d0225d082fd486af629b9804aeb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056203"
---
# <a name="f-volume-shadow-copy-service"></a>F (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F G [H](vssgloss-g.md) [](vssgloss-h.md) [I](vssgloss-i.md) J K [L M](vssgloss-l.md) N [O](vssgloss-n.md) [](vssgloss-o.md) [P P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**componente de grupo de archivos**
</dt> <dd>

Un grupo de archivos distintos de los utilizados como base de datos y definidos por un escritor como que deben controlarse como una unidad durante las operaciones de copia de seguridad y restauración. Vea también componente [*, componente*](vssgloss-c.md)de base [*de datos*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**conjunto de archivos**
</dt> <dd>

Combinación de una ruta de acceso, una especificación de archivo y una marca recursiva que describe uno de los archivos o grupos de archivos. Por ejemplo, los archivos se agregan a los componentes de los conjuntos de archivos.

A menos que se indique lo contrario, las rutas de acceso de un conjunto de archivos son rutas de acceso Windows estándar y pueden contener variables de entorno (por ejemplo, %SystemRoot%) pero no pueden contener caracteres comodín. No es necesario que la ruta de acceso termine con una barra diagonal inversa (" \\ "). Son las aplicaciones las que recuperan esta información para comprobarla.

La especificación de archivo contenida en un conjunto de archivos indica el nombre del archivo o los archivos que incluye. Esta especificación de archivo no puede contener especificaciones de directorio (por ejemplo, sin barras diagonales inversas), pero puede contener ? y \* caracteres comodín.

La etiqueta recursiva es un valor booleano que especifica si la ruta de acceso del conjunto de archivos debe tratarse como un único directorio o si indica una jerarquía de directorios que se recorrerán de forma recursiva. El valor **booleano es true** si la ruta de acceso se trata como una jerarquía de directorios que se recorrerán de forma recursiva, o **false** si no es así.

La información sobre un conjunto de archivos se devuelve a través de instancias de la interfaz **IVssWMFiledesc** y puede contener información adicional que incluye rutas de acceso alternativas, asignaciones de ubicación alternativas y configuración de compatibilidad con esquemas de nivel de archivo.

Vea también ruta [*de acceso alternativa,*](vssgloss-a.md) [*asignación de ubicación alternativa,*](vssgloss-a.md) [*componente*](vssgloss-c.md), *especificación de archivo*.

</dd> <dt>

<span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**especificación de archivo**
</dt> <dd>

Se usa para hacer coincidir los archivos de un directorio y para definir un conjunto de archivos. No puede contener especificaciones de directorio (por ejemplo, sin barras diagonales inversas), pero puede contener el ? y \* caracteres comodín.

</dd> <dt>

<span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Servicio de replicación de archivos**
</dt> <dd>

Se usa para replicar archivos del sistema en un directorio de volumen del sistema redundante (SysVol) para admitir la supervivencia del sistema de archivos, especialmente para sistemas de archivos distribuidos.

</dd> <dt>

<span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**Congelar**
</dt> <dd>

Período de tiempo durante el proceso de creación de instantáneas en el que todos los escritores han vaciado sus escrituras en los volúmenes y no inician escrituras adicionales.

</dd> <dt>

<span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Evento de inmovilización**
</dt> <dd>

Evento de VSS que indica que hay una inmovilización de instantáneas en curso. Consulte también *inmovilizar*, [*instantánea .*](vssgloss-s.md)

</dd> <dt>

<span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**aplicaciones de nivel de front-end**
</dt> <dd>

Indica el punto en el que VSS notifica a un escritor una inmovilización. Los escritores que se inicializaron como aplicaciones de nivel de front-end se notifican antes de que los escritores se inicialicen como aplicaciones de nivel de back-end o como aplicaciones de nivel de sistema. Consulte también [*el nivel de aplicación*](vssgloss-a.md), las aplicaciones de nivel de [*back-end,*](vssgloss-b.md) [*las aplicaciones de nivel de sistema*](vssgloss-s.md)y el [*escritor*](vssgloss-w.md).

</dd> </dl>

 

 



