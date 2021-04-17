---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541715"
---
# <a name="w-volume-shadow-copy-service"></a>W (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [o](vssgloss-o.md) [p](vssgloss-p.md) Q [R](vssgloss-r.md) [s](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z

<dl> <dt>

<span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Protección de archivos de Windows**
</dt> <dd>

Servicio del sistema que protege los archivos especiales del sistema operativo. Si uno de estos archivos se elimina o se sobrescribe, la protección de archivos de Windows reemplaza el archivo por el original de su memoria caché.

</dd> <dt>

<span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**escritor**
</dt> <dd>

Aplicación que coordina sus operaciones de e/s con las operaciones relacionadas con instantáneas y instantáneas de VSS (como copias de seguridad y restauraciones) para que sus datos contenidos en el volumen de la instantánea se encuentren en un estado coherente.

Para admitir esta coordinación, un escritor debe implementar una instancia de una clase derivada de la clase base abstracta **CVssWriter** para comunicarse con la infraestructura de VSS. Consulte también [*instantánea*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**Writer (clase)**
</dt> <dd>

Identificador único global (GUID) proporcionado por un escritor durante la inicialización para indicar que pertenece a un tipo determinado de escritores. Por ejemplo, varias implementaciones de un escritor podrían compartir el mismo identificador de clase del escritor.

Los escritores de la misma clase se pueden distinguir por sus instancias del escritor. Es un desarrollador de aplicaciones quien debe especificar las clases del escritor. Vea también *instancia del escritor*.

</dd> <dt>

<span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**instancia del escritor**
</dt> <dd>

Identificador único global (GUID) proporcionado por VSS para cada proceso de escritura que se ejecuta en un sistema. Cada vez que se inicia el escritor, se genera un valor único para la instancia del escritor.

</dd> <dt>

<span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Documento de metadatos de escritor**
</dt> <dd>

Documento XML creado por un escritor (mediante la interfaz **IVssCreateWriterMetadata** ) que contiene información sobre el estado y los componentes del escritor. Un solicitante puede consultar los documentos de metadatos del escritor (mediante la interfaz **IVssExamineWriterMetadata** ) al realizar una operación de restauración o de copia de seguridad.

Un documento de metadatos de escritor contiene la lista de todos los componentes de un escritor, cualquiera de los cuales puede participar en una copia de seguridad. Esto difiere del documento componentes de copia de seguridad del solicitante, que solo contiene los componentes incluidos explícitamente para una operación de copia de seguridad o restauración.

Una vez construida, el documento de metadatos del escritor debe verse como un objeto de solo lectura. Se puede guardar en el disco. Vea también [*documento componentes de copia de seguridad*](vssgloss-b.md), [*inclusión explícita de componentes*](vssgloss-e.md), [*inclusión implícita de componentes*](vssgloss-i.md).

</dd> </dl>

 

 



